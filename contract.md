# UContract

## Type Contract

### 1. Create Type Contract

#### A. Endpoint

```Javascript
POST /ucontract/api/type-contract
```

#### B. Body

| Field       | Description            |  Type  | Required |
| ----------- | ---------------------- | :----: | :------: |
| name        | Name for Type Contract | String |   Yes    |
| description | Name for Type Contract | String |   Yes    |

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
    id: 3,
    name: 'Contoh Type Contract',
    description: 'Contoh Deskripsi Type Contract'
},
error : null
```

### 2. Update Type Contract

#### A. Endpoint

```Javascript
PUT /ucontract/api/type-contract/:id
```

#### B. Body

| Field       | Description            |  Type  | Required |
| ----------- | ---------------------- | :----: | :------: |
| name        | Name for Type Contract | String |   Yes    |
| description | Name for Type Contract | String |   Yes    |

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
    id: 3,
    name: 'Contoh Type Contract Baru',
    description: 'Contoh Deskripsi Type Contract Baru'
},
error : null
```

### 3. Delete Contract

#### A. Endpoint

```Javascript
DELETE /ucontract/api/contract/:id
```

#### B. Body

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
    id: 3,
    name: 'Contoh Type Contract',
    description: 'Contoh Deskripsi Type Contract'
},
error : null
```

### 4. Get All Type Contract

#### A. Endpoint

```Javascript
GET /ucontract/api/type-contract
```

#### B. Body

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
        id: 6,
        name: 'Contoh Type Contract',
        description: 'Contoh Deskripsi Type Contract'
    },
    {
        id: 7,
        name: 'Contoh Type Contract Lain',
        description: 'Contoh Deskripsi Type Contract Lain'
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

#### B. Body

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

#### C. Request and Response

```Javascript
// Request
{
    no : 'CO1235'
    name : 'Contoh Contract'
    type_contract : 2
    budget : 20000
    vendor : 'Contoh Vendor'
    start_date : '10-11-2023'
    end_date : '10-11-2024'
    scope_of_work : 'Contoh Scope Of Work'
    contract : 'New Contract'
    term_of_payments: [
        {
            term : 'Contoh Term 1',
            percentage: 10.5
        }, {
            term :'Contoh Term 2',
            percentage :89.5
        }
    ]
}
// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message: "Success Create Data",
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
    created_by: 2,
    updated_at: 2023-10-23T21:29:24.192Z,
    created_at: 2023-10-23T21:29:24.192Z
},
error: null
```

### 2. Update Contract

#### A. Endpoint

```Javascript
PUT /ucontract/api/contract/:id
```

#### B. Body

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
    created_by: 2,
    updated_at: 2023-10-23T21:29:24.192Z,
    created_at: 2023-10-23T21:29:24.192Z
},
error : null
```

### 3. Delete Contract

#### A. Endpoint

```Javascript
DELETE /ucontract/api/contract/:id
```

#### B. Body

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

#### B. Body

None

#### C. Request and Response

```Javascript
// Request /ucontract/api/type-contract

// Response
200 OK
httpCode : 200,
httpMessage : 'OK',
message : 'Success Create Data',
data : [
    {
        id: 6,
        name: 'Contoh Type Contract',
        description: 'Contoh Deskripsi Type Contract'
    },
    {
        id: 7,
        name: 'Contoh Type Contract Lain',
        description: 'Contoh Deskripsi Type Contract Lain'
    },
],
error : null
```
