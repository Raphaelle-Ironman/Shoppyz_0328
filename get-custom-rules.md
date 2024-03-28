[service-shoppyz](../../../../README.md) / [API](../README.md) / [custom-rules](./README.md) / Get custom rules

# Get custom rules

Get all custom rules settings by campaign.

```text
GET /campaigns/:id_campaign/rules
```
## Body

| Name   | Description             |
|--------|-------------------------|
| `user` | User doing the request. | 

## Parameters

| Name          | Description        |
|---------------|--------------------|
| `id_campaign` | ID of the campaign.|

## Exemple

```text
GET /campaigns/AiJ34A4j/rules
{
  "user": {
    "id": 1,
    "workspaces": [5],
    "role": "customer"
  }
}
```

Response

```text
200 Ok
```

```json
{
  "custom_rules": [
    {
      "action_type": "increase",
      "id_rule": "6fd6e4a9",
      "action_value": "0.5",
      "rule_name": "test2",
      "conditions": [
        {
          "trigger_dimension": "brand",
          "trigger_value": "eskimo",
          "trigger_condition": "contains"
        },
        {
          "trigger_dimension": "category",
          "trigger_value": "site",
          "trigger_condition": "is"
        }
      ]
    }
  ]
}
```
