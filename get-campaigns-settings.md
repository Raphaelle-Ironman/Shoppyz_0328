[service-shoppyz](../../../../README.md) / [API](../README.md) / [campaign](./README.md) / Get campaigns settings

# Get campaigns settings

Get settings of all campaigns for a customer.

```text
GET /campaigns
```

## Body

| Name   | Description             |
|--------|-------------------------|
| `user` | User doing the request. | 

## Example

```text
GET /campaigns

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
  "data": [
    {
      "name":"nom_campagne_test",
      "id": "iK123jP345",
      "analytics_solution": "ga3",
      "analytics_id": "123",
      "googleads_id": "123",
      "product_feed_type": "xml",
      "product_url_feed": "https://test.xml",
      "shoppyz_url": null,
      "dashboard_url": null,
      "feed_mapping": [
        {
          "name": "id",
          "name_in_feed": "g:id"
        },
        {
          "name": "category",
          "name_in_feed": "g:google_product_category"
        },
        {
          "name": "price",
          "name_in_feed": "g:price"
        }, 
        {
          "name": "item_group_id",
          "name_in_feed": "g:item_group_id"
        }
      ],
      "label_campaign": "0",
      "creation_date": "28 Dec 2023, 11:34:32.595",  
      "scoring_modification_date":"28 Dec 2023, 11:34:32.595",
      "users_emails": ["solene.vinsot@eskimoz.fr"]
    },
  ],
  "last_creation_date": "2024-03-25T16:52:53.835000+00:00",
  "count": 2,
  "page": 1,
  "total": 2,
  "pageCount": 1
}
```
