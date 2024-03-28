[service-shoppyz](../../../../README.md) / [API](../README.md) / [how-to-use](./README.md) / Filter
# Sort

All collections routes `SHOULD` have a filter system.

## query rules

- query `MUST` have a variable named `q`. this variable is a json object.
- to sort filter, q `MUST` contain `filter` as key which is a dictionnary
- `filter` contains `$or` as key with a list of filters
- each filter has the name of field to filter and contains `$like` if the condition is "contains" and the value to filter

## exemple

```
GET /campaigns?q={"filter":{"$or":[{"name":{"$like":"Es"}},{"name":{"$like":"Senek"}}]}}
```

```json
{
  "data": [
    {
      "id": "0b955cd9-b14b-41d2-8f3b-2164022b3534",
      "name": "Eskimoz",
      "creation_date": "2024-03-25T17:52:18.183000+00:00"
    }, 
    {
      "id": "18cb1aa0-58fb-49c5-9b20-0d9ab8d5a88e",
      "name": "Senek",
      "creation_date": "2024-03-25T17:52:18.183000+00:00"
    }, 
    {
      "id": "18cb1aa0-58fb-49c5-9b20-0d9ab8d5a88e",
      "name": "Senek",
      "creation_date": "2024-03-24T17:52:18.183000+00:00"
    }
  ]
}
```