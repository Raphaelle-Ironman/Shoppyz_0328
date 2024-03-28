[service-shoppyz](../../../../README.md) / [API](../README.md) / [campaign](./README.md) / Delete a customer

# Delete a customer

Delete a customer.

```text
DELETE /campaigns
```

## Body

| Name   | Description             |
|--------|-------------------------|
| `user` | User doing the request. | 

## Parameters

| Name          | Description         |
|---------------|---------------------|
| `id_campaign` | ID of the campaign. |

## Example

```text
DELETE /campaigns

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
200 OK
```
