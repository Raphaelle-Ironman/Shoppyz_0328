[service-shoppyz](../../../../README.md) / [API](../README.md) / [dashboard](./README.md) / Modify a dashboard

# modify a dashboard

Add dashboard url to campaign settings.

```text
PUT /campaigns/:id_campaign/dashboard
```

## Body

| Name                | Description                         |
|---------------------|-------------------------------------|
| `user`              | User doing the request.             | 
| `dashboard_url`     | URL of the looker studio dashboard. |


## Parameters

| Name          | Description         |
|---------------|---------------------|
| `id_campaign` | ID of the campaign. |

## Example

```text
PUT /campaigns/AWJoU0w4hk6gVoEMN4lS/dashboard

{ 
  "user": {
    "id": "123",
    "workspaces": [5],
    "role": "customer"
  },
  "dashboard_url": "https://url_test_looker.test"
}

```

Response

```text
200 Ok
```

```json
{
  "user": {
    "workspaces": [
      5
    ],
    "role": "customer",
    "id": "123"
  },
  "dashboard_url": "https://url_test_looker.test"
}
```
