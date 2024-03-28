[service-shoppyz](../../../../README.md) / [API](../README.md) / [scoring](./README.md) / Get scoring

# Get scoring

Get scores by kpis

```text
GET /campaigns/:id_campaign/scoring
```

## Body

| Name   | Description             |
|--------|-------------------------|
| `user` | User doing the request. | 

## Parameters

| Name          | Description        |
|---------------|--------------------|
| `id_campaign` | ID of the campaign.|

## Example

```text
GET /campaigns/iK123jP345/scoring

{ 
  "user": {
    "id": 1,
    "workspaces": [5],
    "role": "customer"
  }
}
```

Response

```json
{ 
  "scoring_modification_date":"28 Dec 2023, 11:34:32.595",
  "shoppyz_url": "",
  "kpis": ["sessions","conversions"],
  "scores": ["0.2","0.8"]
}
```
