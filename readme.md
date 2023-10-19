# Udream

Add Ideation Payload Example :
```json
{
    "ideation_name": "Sopoline Richards",
    "ideation_date": "2017-01-15",
    "requestor_nik": 712812,
    "candidates" : [1],
    "intangible_benefit": [
        {
            "questionId": 2,
            "value": [
                {
                  "details" : "Contoh Detail Intangible"
                },
                {
                  "details" : "Contoh Detail Intangible 2"
                },
                false,
                {
                  "others" : "Contoh Others",
                  "details" : "Contoh Detail Intangible 3"
                },
                false
            ]
        }
    ],
    "tangible_benefit": [
        {
            "questionId": 4,
            "value": [
                {
                    "details" : "Contoh Detail Tangible 1"
                },
                {
                    "details" : "Contoh Detail Tangible 2"
                },
                false
            ]
        },
        {
            "questionId": 3,
            "value": "HIGH",
            "details": "lorem ipsum"
        }
    ],
    "time_delivery": [
        {
            "questionId": 6,
            "value": "HIGH",
            "details": "lorem ipsum"
        }
    ],
    "objective": "lorem ipsum"
}
```

Validate Payload Example :

```json
{
  "ideation_id" : 1,
  "ideation_date" : "10-11-2023",
  "ideation_name" : "Contoh Ideation",
  "objective" : "Contoh Objective",
  "project_scope" : "Contoh Scope",
  "project_cost" : 500_000,
  "project_duration" : 10,
  "project_milestone" : 10,
  "deliverables" : "Contoh Delivearables",
  "budget_code" : "Contoh Budget Code",
  "project_risk" : "Contoh Project Risk",
  "with_poc" : true,
}
```

Create Quesioner By GentaGendis
```json
{
    "gen_id" : 12, // Id Genta Gendis
    "ideation_id" : 1,
    "quesioner_id" : 2,
    "intangible_benefit": [
        {
            "questionId": 2,
            "value": [
                {
                  "details" : "Contoh Detail Intangible"
                },
                {
                  "details" : "Contoh Detail Intangible 2"
                },
                false,
                {
                  "others" : "Contoh Others",
                  "details" : "Contoh Detail Intangible 3"
                },
                false
            ]
        }
    ],
    "tangible_benefit": [
        {
            "questionId": 4,
            "value": [
                {
                    "details" : "Contoh Detail Tangible 1"
                },
                {
                    "details" : "Contoh Detail Tangible 2"
                },
                false
            ]
        },
        {
            "questionId": 3,
            "value": "HIGH",
            "details": "lorem ipsum"
        }
    ],
    "time_delivery": [
        {
            "questionId": 6,
            "value": "HIGH",
            "details": "lorem ipsum"
        }
    ],
}
```