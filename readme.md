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
    "objective": "lorem ipsum"
}
```

Validate Payload Example :

```json
{
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