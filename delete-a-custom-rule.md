[service-shoppyz](../../../../README.md) / [API](../README.md) / [custom-rules](./README.md) / Delete a custom rule

# Delete a custom rule

Delete a custom rule

```text
DELETE /campaigns/:id_campaign/rules/:id_rule
```

## Body

| Name   | Description             |
|--------|-------------------------|
| `user` | User doing the request. | 

## Parameters

| Name          | Description        |
|---------------|--------------------|
| `id_campaign` | ID of the campaign.|
| `id_rule`     | ID of the rule.    |

## Exemple

```text
DELETE /campaigns/AiJ34A4j/rules/hM45i90

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
