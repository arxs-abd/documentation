# UContract

## Type Contract

### 1. Create Type Contract

#### A. Endpoint

```Javascript
POST /ucontract/api/type-contract
```

#### B. Body, Params, and Query

##### Body

| Field       | Description            |  Type  | Required |
| ----------- | ---------------------- | :----: | :------: |
| name        | Name for Type Contract | String |   Yes    |
| description | Name for Type Contract | String |   Yes    |

##### Params

None

##### Query

None

#### C. Request and Response

```Javascript
// Request
{
    name : 'Contoh Type Contract',
    description : 'Contoh Deskripsi Type Contract',
}
// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message: 'Success Create Data',
data: {
    id : 3,
    name : 'Contoh Type Contract',
    description : 'Contoh Deskripsi Type Contract'
},
error : null
```

### 2. Update Type Contract

#### A. Endpoint

```Javascript
PUT /ucontract/api/type-contract/:id
```

#### B. Body, Params, and Query

##### Body

| Field       | Description            |  Type  | Required |
| ----------- | ---------------------- | :----: | :------: |
| name        | Name for Type Contract | String |   Yes    |
| description | Name for Type Contract | String |   Yes    |

##### Params

None

##### Query

None

#### C. Request and Response

```Javascript
// Request : /ucontract/api/type-contract/3
{
    name : 'Contoh Type Contract Baru',
    description : 'Contoh Deskripsi Type Contract Baru',
}
// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message : 'Success Update Data',
data : {
    id : 3,
    name : 'Contoh Type Contract Baru',
    description : 'Contoh Deskripsi Type Contract Baru'
},
error : null
```

### 3. Delete Contract

#### A. Endpoint

```Javascript
DELETE /ucontract/api/contract/:id
```

#### B. Body, Params, and Query

##### Body

None

##### Params

None

##### Query

None

#### C. Request and Response

```Javascript
// Request /ucontract/api/type-contract/3

// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message : 'Success Delete Data',
data : {
    id : 3,
    name : 'Contoh Type Contract',
    description : 'Contoh Deskripsi Type Contract'
},
error : null
```

### 4. Get All Type Contract

#### A. Endpoint

```Javascript
GET /ucontract/api/type-contract
```

#### B. Body, Params, and Query

##### Body

None

##### Params

None

##### Query

None

#### C. Request and Response

```Javascript
// Request /ucontract/api/type-contract

// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message : 'Success Get All Data',
data : [
    {
        id : 6,
        name : 'Contoh Type Contract',
        description : 'Contoh Deskripsi Type Contract'
    },
    {
        id : 7,
        name : 'Contoh Type Contract Lain',
        description : 'Contoh Deskripsi Type Contract Lain'
    },
],
error : null
```

## Contract

### 1. Create Contract

#### A. Endpoint

```Javascript
POST /ucontract/api/contract
```

#### B. Body, Params, and Query

##### Body

| Field            | Description                                  |           Type           |           Required            |
| ---------------- | -------------------------------------------- | :----------------------: | :---------------------------: |
| name             | Name for Type Contract                       |          String          |              Yes              |
| no               | Number of Contract                           |          String          |              Yes              |
| type_contract    | Type of Contract                             |          String          |              Yes              |
| budget           | Budget of Contract                           |          String          |              Yes              |
| remaining_budget | Remaining Budget of Contract                 |          String          | Yes (If contract is On Going) |
| vendor           | Vendor of Contract                           |          String          |              Yes              |
| start_date       | Start Date of Contract                       |          String          |              Yes              |
| end_date         | End Date of Contract                         |          String          |              Yes              |
| scope_of_work    | Scope Of Work in Contract                    |          String          |              Yes              |
| contract         | Status in Contract                           | (New Contract, On Going) |              Yes              |
| contract_owner   | Owner in Contract                            |           Int            |              Yes              |
| term_of_payments | Term of Payments of Contract                 |          Object          |              Yes              |
| email_cc         | CC Email for Notification of Contract        |          Object          |              Yes              |
| email_bcc        | BCC Email for Notification of Contract       |          Object          |              Yes              |
| whatsapp_number  | Whatsapp Number for Notification of Contract |          Object          |              Yes              |
| notification     | Notification Setting for Contract            |          Object          |              Yes              |
| files            | Document for Contract                        |           File           |              Yes              |

##### Params

None

##### Query

None

#### C. Request and Response

```Javascript
// Request
{
    no : 'CO1235'
    name : 'Contoh Contract'
    type_contract : 2
    budget : 20000
    vendor : 'Contoh Vendor'
    start_date : '2023-11-10'
    end_date : '2024-11-10'
    scope_of_work : 'Contoh Scope Of Work'
    contract : 'New Contract'
    term_of_payments: [
        {
            term : 'Contoh Term 1',
            percentage : 10.5
        }, {
            term : 'Contoh Term 2',
            percentage : 89.5
        }
    ]
    email_cc : ['contoh@email.com']
    email_bcc : ['contoh1@email.com']
    whatsapp_number : ['+6288888888888']
    notification : [
        {
            notification_id : 1
            email_active : true
            whatsapp_active : true
        }, {
            notification_id : 2
            email_active : false
            whatsapp_active : true
        }
    ]
}
// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message: 'Success Create Data',
data : {
    id : 19,
    no : 'CO1235'
    name : 'Contoh Contract'
    type_contract : 2
    budget : 20000
    vendor : 'Contoh Vendor'
    start_date : '10-11-2023'
    end_date : '10-11-2024'
    scope_of_work : 'Contoh Scope Of Work'
    contract : 'New Contract'
    scope_of_work : 'Sangat Jauh Sekali',
    term_of_payments : '[{\"term\":\"DP nya saja\",\"percentage\":10.5},{\"term\":\"Sisanya\",\"percentage\":89.5}]',
    files : '[\"1698125364186-picture-large.jpg\",\"1698125364186-picture-small.jpg\"]',
    status : 'On Going',
    email_cc : ['contoh@email.com']
    email_bcc : ['contoh1@email.com']
    whatsapp_number : ['+6288888888888']
    created_by : 2,
    updated_at : 2023-10-23T21:29:24.192Z,
    created_at : 2023-10-23T21:29:24.192Z
},
error : null
```

### 2. Update Contract

#### A. Endpoint

```Javascript
PUT /ucontract/api/contract/:id
```

#### B. Body, Params, and Query

##### Body

| Field            | Description                  |           Type           |           Required            |
| ---------------- | ---------------------------- | :----------------------: | :---------------------------: |
| name             | Name for Type Contract       |          String          |              Yes              |
| no               | Number of Contract           |          String          |              Yes              |
| type_contract    | Type of Contract             |          String          |              Yes              |
| budget           | Budget of Contract           |          String          |              Yes              |
| remaining_budget | Remaining Budget of Contract |          String          | Yes (If contract is On Going) |
| vendor           | Vendor of Contract           |          String          |              Yes              |
| start_date       | Start Date of Contract       |          String          |              Yes              |
| end_date         | End Date of Contract         |          String          |              Yes              |
| scope_of_work    | Scope Of Work in Contract    |          String          |              Yes              |
| contract         | Status in Contract           | (New Contract, On Going) |              Yes              |
| term_of_payments | Term of Payments of Contract |          Object          |              Yes              |
| files            | Document for Contract        |           File           |              Yes              |

##### Params

None

##### Query

None

#### C. Request and Response

```Javascript
// Request : /ucontract/api/type-contract/19
{
    no : 'CO1235'
    name : 'Contoh Contract Terbaru'
    type_contract : 2
    budget : 200000
    vendor : 'Contoh Vendor'
    start_date : '10-11-2023'
    end_date : '10-11-2024'
    scope_of_work : 'Contoh Scope Of Work Terbaru'
    contract : 'New Contract'
    term_of_payments: [
        {
            term : 'Contoh Term 1',
            percentage: 10.5
        }, {
            term :'Contoh Term 2',
            percentage :89.5
        }
    ],
    files : 'Upload Document For Contract'
}
// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message: 'Success Update Data',
data : {
    id : 19,
    no : 'CO1235'
    name : 'Contoh Contract Terbaru'
    type_contract : 2
    budget : 200000
    vendor : 'Contoh Vendor'
    start_date : '10-11-2023'
    end_date : '10-11-2024'
    scope_of_work : 'Contoh Scope Of Work Terbaru'
    contract : 'New Contract'
    scope_of_work : 'Sangat Jauh Sekali',
    term_of_payments : '[{\"term\":\"DP nya saja\",\"percentage\":10.5},{\"term\":\"Sisanya\",\"percentage\":89.5}]',
    files : '[\"1698125364186-picture-large.jpg\",\"1698125364186-picture-small.jpg\"]',
    status : 'On Going',
    created_by : 2,
    updated_at : 2023-10-23T21:29:24.192Z,
    created_at : 2023-10-23T21:29:24.192Z
},
error : null
```

### 3. Delete Contract

#### A. Endpoint

```Javascript
DELETE /ucontract/api/contract/:id
```

#### B. Body, Params, and Query

##### Body

None

##### Params

None

##### Query

| Field  | Description              |          Type           | Required |
| ------ | ------------------------ | :---------------------: | :------: |
| status | Status of Contract       |         String          |    No    |
| page   | Page for Pagination      |  Number (Default : 1)   |    No    |
| size   | Size per Page Pagination | Number (Default : 1000) |    No    |

#### C. Request and Response

```Javascript
// Request /ucontract/api/type-contract/3

// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message : 'Success Delete Data',
data : {
    id : 3,
    name : 'Contoh  Contract',
    description : 'Contoh Delete Contract'
},
error : null
```

### 4. Get All Contract

#### A. Endpoint

```Javascript
GET /ucontract/api/contract
```

#### B. Body, Params, and Query

##### Body

None

##### Params

None

##### Query

None

#### C. Request and Response

```Javascript
// Request /ucontract/api/contract

// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message : 'Success Get Data',
data : [
    {
        no : 'CO1235',
        name : 'Contoh Contract 1235',
        status : 'On Going',
        scope_of_work : 'Contoh Scope Of Work',
        typeContract : {
            id : 2,
            name : 'Contoh Type Contract 2',
            description : 'Contoh Type Contract Deskripsi 2'
        }
    },
    {
        no : 'CO1237',
        name : 'Contoh Contract 1237',
        status : 'On Going',
        scope_of_work : 'Contoh Scope Of Work',
        typeContract : {
            id : 4,
            name : 'Contoh Type Contract 4',
            description : 'Contoh Type Contract Deskripsi 4'
        }
    }
],
error : null
```

### 5. Import Contract From Excel

#### A. Endpoint

```Javascript
GET /ucontract/api/contract/import
```

#### B. Body, Params, and Query

##### Body

None

##### Params

None

##### Query

None

#### C. Request and Response

```Javascript
// Request /ucontract/api/contract/export

// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message : 'Success Import Data',
data : null,
error : null
```

## Notification Type

### 1. Get All Notification Type

#### A. Endpoint

```Javascript
GET /ucontract/api/type-notif
```

#### B. Body, Params, and Query

##### Body

None

##### Params

None

##### Query

None

#### C. Request and Response

```Javascript
// Request /ucontract/api/type-notif

// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message : 'Success Get All Data',
data : [
    {
        id: 1,
        name: 'Create Contract',
        email_template: 'Tes Templatenya'
    }
],
error : null
```

### 2. Get Notification Type By ID

#### A. Endpoint

```Javascript
GET /ucontract/api/type-notif/:id
```

#### B. Body, Params, and Query

##### Body

None

##### Params

| Field | Description             | Required |
| ----- | ----------------------- | :------: |
| id    | ID of Notification Type |   Yes    |

##### Query

None

#### C. Request and Response

```Javascript
// Request /ucontract/api/type-notif/1

// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message : 'Success Get Data',
data :{
    id: 1,
    name: 'Create Contract',
    email_template: 'Tes Templatenya'
},
error : null
```

### 3. Create Notification Type

#### A. Endpoint

```Javascript
POST /ucontract/api/type-notif/
```

#### B. Body, Params, and Query

##### Body

| Field          | Description                          |  Type  | Required |
| -------------- | ------------------------------------ | :----: | :------: |
| name           | Name of Notification Type            | String |   Yes    |
| subject        | Subject EMail of Notification Type   | String |   Yes    |
| email_template | Template Email for Notification Type | String |   Yes    |

##### Params

None

##### Query

None

#### C. Request and Response

```Javascript
// Request /ucontract/api/type-notif/
{
    name: 'Create Contract',
    email_template: 'Tes Templatenya'
}

// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message : 'Success Create Data',
data :{
    id: 1,
    name: 'Create Contract',
    email_template: 'Tes Templatenya'
},
error : null
```

### 4. Update Notification Type

#### A. Endpoint

```Javascript
PUT /ucontract/api/type-notif/:id
```

#### B. Body, Params, and Query

##### Body

| Field          | Description                          |  Type  | Required |
| -------------- | ------------------------------------ | :----: | :------: |
| name           | Name of Notification Type            | String |   Yes    |
| subject        | Subject Email for Notification Type  | String |   Yes    |
| email_template | Template Email for Notification Type | String |   Yes    |

##### Params

| Field | Description             | Required |
| ----- | ----------------------- | :------: |
| id    | ID of Notification Type |   Yes    |

##### Query

None

#### C. Request and Response

```Javascript
// Request /ucontract/api/type-notif/1
{
    name: 'Create Contract Lagi',
    email_template: 'Tes Templatenya Lagi'
}

// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message : 'Success Update Data',
data :{
    id: 1,
    name: 'Create Contract Lagi',
    email_template: 'Tes Templatenya Lagi'
},
error : null
```

### 5. Delete Notification Type

#### A. Endpoint

```Javascript
DELETE /ucontract/api/type-notif/:id
```

#### B. Body, Params, and Query

##### Body

None

##### Params

| Field | Description             | Required |
| ----- | ----------------------- | :------: |
| id    | ID of Notification Type |   Yes    |

##### Query

None

#### C. Request and Response

```Javascript
// Request /ucontract/api/type-notif/1

// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message : 'Success Delete Data',
data :{
    id: 1,
    name: 'Create Contract Lagi',
    email_template: 'Tes Templatenya Lagi'
},
error : null
```

## Notification

### 1. Get All Notification

#### A. Endpoint

```Javascript
GET /ucontract/api/notification
```

#### B. Body, Params, and Query

##### Body

None

##### Params

None

##### Query

None

#### C. Request and Response

```Javascript
// Request /ucontract/api/notifnotification

// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message : 'Success Get All Data',
data : [
    {
        id : 1,
        title : 'Contoh Notif',
        notification_type_id : 2,
        notification_time : null,
        budget_notification : 10,
        subject : null,
        cc : ['contoh@email.com'],
        bcc : ['contoh2@email.com'],
        template : 'Contoh Template',
        created_at : '2023-11-14T19:59:59.699Z',
        updated_at : '2023-11-14T19:59:59.699Z',
        type_notification: {
            id : 2,
            name : 'Create Contract',
            email_template: 'Tes Templatenya'
        }
    },
],
error : null
```

### 2. Get Notification By ID

#### A. Endpoint

```Javascript
GET /ucontract/api/notification/:id
```

#### B. Body, Params, and Query

##### Body

None

##### Params

| Field | Description        | Required |
| ----- | ------------------ | :------: |
| id    | ID of Notification |   Yes    |

##### Query

None

#### C. Request and Response

```Javascript
// Request /ucontract/api/notifnotification/1

// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message : 'Success Get Data',
data : {
        id : 1,
        title : 'Contoh Notif',
        notification_type_id : 2,
        notification_time : null,
        budget_notification : 10,
        subject : null,
        cc : ['contoh@email.com'],
        bcc : ['contoh2@email.com'],
        template : 'Contoh Template',
        created_at : '2023-11-14T19:59:59.699Z',
        updated_at : '2023-11-14T19:59:59.699Z',
        type_notification: {
            id : 2,
            name : 'Create Contract',
            email_template: 'Tes Templatenya'
    }
},
error : null
```

### 3. Create Notification

#### A. Endpoint

```Javascript
POST /ucontract/api/notification
```

#### B. Body, Params, and Query

##### Body

| Field                | Description                                                     |  Type  |             Required              |
| -------------------- | --------------------------------------------------------------- | :----: | :-------------------------------: |
| title                | Title of Notification                                           | String |                Yes                |
| notification_type_id | Template Email for Notification Type                            |  Int   |                Yes                |
| notification_time    | Time to Run Notification By End Date                            |  Int   | Yes (If budget_notification null) |
| budget_notification  | Budget Percentage for Remaining Budget Notification By End Date |  Int   |  Yes (If notification_time null)  |
| cc                   | CC of Email in Notification                                     | Array  |                Yes                |
| bcc                  | BCC of Email in Notification                                    | Array  |                Yes                |
| template             | Template Email for Notification                                 | String |                Yes                |

##### Params

None

##### Query

None

#### C. Request and Response

```Javascript
// Request /ucontract/api/notifnotification
{
    title : 'Contoh Notif',
    notification_type_id : 2,
    notification_time : null,
    budget_notification : 30,
    subject : 'Contoh Subject',
    template : 'Contoh Template',
}

// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message : 'Success Create Data',
data : {
        id : 1,
        title : 'Contoh Notif',
        notification_type_id : 2,
        notification_time : null,
        budget_notification : 10,
        subject : null,
        subject : 'Contoh Subject',
        template : 'Contoh Template',
        created_at : '2023-11-14T19:59:59.699Z',
        updated_at : '2023-11-14T19:59:59.699Z',
        type_notification: {
            id : 2,
            name : 'Create Contract',
            email_template: 'Tes Templatenya'
    }
},
error : null
```

### 4. Update Notification

#### A. Endpoint

```Javascript
PUT /ucontract/api/notification
```

#### B. Body, Params, and Query

##### Body

| Field                | Description                                                     |  Type  |             Required              |
| -------------------- | --------------------------------------------------------------- | :----: | :-------------------------------: |
| title                | Title of Notification                                           | String |                Yes                |
| notification_type_id | Template Email for Notification Type                            |  Int   |                Yes                |
| notification_time    | Time to Run Notification By End Date                            |  Int   | Yes (If budget_notification null) |
| budget_notification  | Budget Percentage for Remaining Budget Notification By End Date |  Int   |  Yes (If notification_time null)  |
| cc                   | CC of Email in Notification                                     | Array  |                Yes                |
| bcc                  | BCC of Email in Notification                                    | Array  |                Yes                |
| template             | Template Email for Notification                                 | String |                Yes                |

##### Params

| Field | Description        | Required |
| ----- | ------------------ | :------: |
| id    | ID of Notification |   Yes    |

##### Query

None

#### C. Request and Response

```Javascript
// Request /ucontract/api/notifnotification/1
{
    title : 'Contoh Notif Contoh',
    notification_type_id : 2,
    notification_time : null,
    budget_notification : 30,
    subject : 'Contoh Subject',
    template : 'Contoh Template',
}

// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message : 'Success Update Data',
data : {
        title : 'Contoh Notif Contoh',
        notification_type_id : 2,
        notification_time : null,
        budget_notification : 30,
        subject : 'Contoh Subject',
        template : 'Contoh Template',
        created_at : '2023-11-14T19:59:59.699Z',
        updated_at : '2023-11-14T19:59:59.699Z',
        type_notification: {
            id : 2,
            name : 'Create Contract',
            email_template: 'Tes Templatenya'
    }
},
error : null
```

### 5. Delete Notification

#### A. Endpoint

```Javascript
DELETE /ucontract/api/notification/:id
```

#### B. Body, Params, and Query

##### Body

None

##### Params

| Field | Description        | Required |
| ----- | ------------------ | :------: |
| id    | ID of Notification |   Yes    |

##### Query

None

#### C. Request and Response

```Javascript
// Request /ucontract/api/notifnotification/1

// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message : 'Success Remove Data',
data : {
        id : 1,
        title : 'Contoh Notif',
        notification_type_id : 2,
        notification_time : null,
        budget_notification : 10,
        subject : null,
        cc : ['contoh@email.com'],
        bcc : ['contoh2@email.com'],
        template : 'Contoh Template',
        created_at : '2023-11-14T19:59:59.699Z',
        updated_at : '2023-11-14T19:59:59.699Z',
        type_notification: {
            id : 2,
            name : 'Create Contract',
            email_template: 'Tes Templatenya'
    }
},
error : null
```

## VENDOR

### 1. Get All Vendor

#### A. Endpoint

```Javascript
GET /ucontract/api/vendor
```

#### B. Body, Params, and Query

##### Body

None

##### Params

None

##### Query

None

#### C. Request and Response

```Javascript
// Request /ucontract/api/vendor

// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message : 'Success Get Data',
data : [
    'A ZAKI [100000]',
    'ABADI JAYA [100001]',
    'ABIDIN JETTY - TABONEO [100002]',
    'ACNAZ CELLULER [100003]',
    'ACRYLAND, PT [100004]',
    'AD REKSA DATA INTI, PT [100005]',
    'ADI SARANA [100006]',
    'ADI SARANA ARMADA TBK, PT (ASSARENT) [100007]',
    'ADVANCE TECHNOLOGY COMPUTER [100008]',
    'MUHAMMAD ARIEF BUDIMAN (AFWAJA) [100009]',
    'LIE LIE (AGRO TEKNIK) [100010]',
    'AGUNG RADIATOR [100011]',
    'AHMAD YUSUF [100012]',
    'AIRBORNE INFORMATICS, PT [100013]',
    'AL MUNSJAH [100014]',
    ...
],
error : null
```
