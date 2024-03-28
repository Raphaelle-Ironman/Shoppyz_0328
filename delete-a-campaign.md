[service-shoppyz](../../../../README.md) / [API](../README.md) / [campaign](./README.md) / Delete a campaign

# Delete a campaign

Delete a campaign.

```text
DELETE /campaigns/:id_campaign
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
DELETE /campaigns/iK123jP345

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
