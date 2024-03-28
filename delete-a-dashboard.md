[service-shoppyz](../../../../README.md) / [API](../README.md) / [dashboard](./README.md) / Delete a dashboard

# Delete a dashboard

Add dashboard url to campaign settings.

```text
DELETE /campaigns/:id_campaign/dashboard
```

## Body

| Name                | Description                         |
|---------------------|-------------------------------------|
| `user`              | User doing the request.             | 


## Parameters

| Name          | Description         |
|---------------|---------------------|
| `id_campaign` | ID of the campaign. |

## Example

```text
DELETE /campaigns/AWJoU0w4hk6gVoEMN4lS/dashboard

{ 
  "user": {
    "id": "123",
    "workspaces": [5],
    "role": "customer"
  }
}

```

Response

```text
200 Ok
```
