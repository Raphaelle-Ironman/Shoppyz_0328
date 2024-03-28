[service-shoppyz](../../../../README.md) / [API](../README.md) / [campaign](./README.md) / Get shopping feed url

# Get shopping feed url

Get a googlesheet url.

```text
GET /campaigns/:id_campaign/url
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
GET /campaigns/Ajk23Mj5/url

{
  "user": {
    "id": 1,
    "workspaces": [5],
    "role": "customer"
  }
}
```

Response:

```json
{
  "url": "https://docs.google.com/spreadsheets/d/123/edit#gid=123"
}
```
