[service-shoppyz](../../../../README.md) / [API](../README.md) / [custom-rules](./README.md) / Add a custom rule

# Add a custom rule

Add custom rule setup.

```text
PUT /campaigns/:id_campaign/rules
```

## Body

| Name                | Description                                             |
|---------------------|---------------------------------------------------------|
| `user`              | User doing the request.                                 | 
| `rule_name`         | Name of the custom rule                                 |
| `conditions`        | list of triggers containing dimension, value, condition |
| `trigger_dimension` | Dimension of the trigger, lowercase                     |
| `trigger_condition` | Condition of the trigger, lowercase                     |
| `trigger_value`     | Value condition of the trigger, lowercase or float      |
| `action_type`       | Type of action, lowercase                               |
| `action_value`      | Value of action, lowercase or float.                    |

## Parameters

| Name          | Description         |
|---------------|---------------------|
| `id_campaign` | ID of the campaign. |

## Example

```text
PUT /campaigns/AiJ34A4j/rules

{ 
  "user": {
    "id":0,
    "workspaces": [5]
  },
  "rule_name":"test2",
  "conditions": [
    {
      "trigger_dimension": "brand",
      "trigger_condition": "contains",
      "trigger_value": "eskimo"
    },
    {
      "trigger_dimension": "category",
      "trigger_condition": "is",
      "trigger_value": "site"}     
  ],
  "action_type": "increase",
  "action_value":"0.5"
}

```

Response

```text
200 Ok
```

```json
{
  "user": {
    "id": 0,
    "workspaces": [
      5
    ]
  },
  "rule_name": "test2",
  "conditions": [
    {
      "trigger_dimension": "brand",
      "trigger_condition": "contains",
      "trigger_value": "eskimo"
    },
    {
      "trigger_dimension": "category",
      "trigger_condition": "is",
      "trigger_value": "site"
    }
  ],
  "action_type": "increase",
  "action_value": "0.5"
}

```
