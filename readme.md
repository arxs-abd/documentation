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

Add Quesioner From Genta/Gendis By Ideation Example :

```json
{
    "quesioner_id": 3,
    "gen_id": 5,
    "ideation_id": 2,
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