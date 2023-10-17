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
          "questionId": 3,
          "value": [
            {
              "details" : "Contoh Detail"
            },
            {
              "details" : "Contoh Detail 2"
            },
            false, // If User Not Select
            {
              "others" : "Contoh Others", // If Users select Others
              "details" : "Bla Bla Bla"
            },
            false
          ], // For Multiple Choices
        },
    ],
    "tangible_benefit": [
        {
          "questionId": 1,
          "value": "HIGH",
          "reason": "lorem ipsum",
        },
        {
          "questionId": 5,
          "value": 1,
          "reason": "lorem ipsum",
        },
    ],
    "time_delivery": [
        {
          "questionId": 124,
          "value": "HIGH",
          "reason": "lorem ipsum",
        },
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
        "questionId": 3,
        "value": [true, true, true, false], // For Multiple Choices
        "reason": "lorem ipsum",
      },
  ],
  "tangible_benefit": [
      {
        "questionId": 1,
        "value": "HIGH",
        "reason": "lorem ipsum",
      },
      {
        "questionId": 5,
        "value": 1,
        "reason": "lorem ipsum",
      },
  ],
  "time_delivery": [
      {
        "questionId": 124,
        "value": "HIGH",
        "reason": "lorem ipsum",
      },
  ],
}
```