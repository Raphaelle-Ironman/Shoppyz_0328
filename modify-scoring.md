[service-shoppyz](../../../../README.md) / [API](../README.md) / [scoring](./README.md) / Modify scoring


# Modify scoring

Modify kpis and scores setup.

```text
PUT /campaigns/:id_campaign/scoring
```

## Body

| Name     | Description                |
|----------|----------------------------|
| `user`   | User doing the request.    | 
| `kpis`   | List of kpis to be scored. |
| `scores` | List of scores.            |

## Parameters

| Name          | Description        |
|---------------|--------------------|
| `id_campaign` | ID of the campaign.|

## Example

```text
PUT /campaigns/iK123jP345/scoring

{ 
  "user": {
    "id": 1,
    "workspaces": [5],
    "role": "customer"
  },
  "kpis": ["sessions","conversions"],
  "scores": ["0.2","0.8"]
}

```

Response

```text
200 Ok
```

```json
{ 
  "kpis": ["sessions","conversions"],
  "scores": ["0.2","0.8"]
}

```
