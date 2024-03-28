[service-shoppyz](../../../../README.md) / [API](../README.md) / [how-to-use](./README.md) / Sort
# Sort

All collections routes `SHOULD` have a sort system.

## query rules

- query `MUST` have a variable named `q`. this variable is a json object.
- to sort data, q `MUST` contain `sort` as key and a list of dict with name and sort condition.
- to sort ascending, sort condition `MUST` be `asc`
- to sort descending, sort condition `MUST` be `dsc`
- order of sort conditions in `sort` list has importance

## exemple

```
GET /campaigns?q={"sort": [{ "creation_date": "dsc" }, { "name": "asc" }]}
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