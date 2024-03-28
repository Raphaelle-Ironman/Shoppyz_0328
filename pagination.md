[service-shoppyz](../../../../README.md) / [API](../README.md) / [how-to-use](./README.md) / Pagination
# Pagination

All collections routes `MUST` have a pagination system.

## response rules

- data list `MUST` have `data` as key in json response.
- response `MUST` contains keys to describe the page property :
  - `count`    : number of results in the actual page.
  - `page`     : numero of actual page. Beginning by one.
  - `total`    : total number of results.
  - `pageCount`: total number of pages.

## query rules

- query `MUST` have a variable named `q`. this variable is a json object.
- to select page, `q MUST` contain `page` as key and an integer beginning by `one` as value.
- to select the number of results by page, `q MUST` contain `amount` as key and a positive integer as value.

## exemple

```
GET /clients?q={"amount":2,"page":3}
```

```json
{
  "data": [{
    "id": "0b955cd9-b14b-41d2-8f3b-2164022b3534",
    "name": "Eskimoz"
  }, {
    "id": "18cb1aa0-58fb-49c5-9b20-0d9ab8d5a88e",
    "name": "Senek"
  }],
  "count": 2,
  "page": 3,
  "total": 11,
  "pageCount": 6
}
```