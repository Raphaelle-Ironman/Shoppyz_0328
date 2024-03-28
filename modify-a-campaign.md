[service-shoppyz](../../../../README.md) / [API](../README.md) / [campaign](./README.md) / Modify a campaign

# Modify a campaign

Modify a campaign, starting scoring with setting score.

```text
PUT /campaigns/:id_campaign
```

## Body

| Name                               | Description                                              |
|------------------------------------|----------------------------------------------------------|
| `user`                             | User doing the request.                                  | 
| `analytics_solution`               | Choice of Analytics version.                             |
| `analytics_id`                     | Analytics ID                                             |
| `googleads_id`                     | Google Ads ID                                            |
| `product_feed_type`                | Type of product feed                                     |
| `product_url_feed`                 | URL of the feed                                          |
| `feed_mapping`                     | List name and name_in_feed to map product feed.          |
| `label_campaign`                   | Label between 0 and 4 for the campaign.                  |

## Parameters

| Name          | Description         |
|---------------|---------------------|
| `id_campaign` | ID of the campaign. |

## Example

```text
PUT /campaigns/iK123jP345

{
  "user": {
    "id": 1,
    "workspaces": [5],
    "role": "customer"
  },
  "analytics_solution": "ga3",
  "analytics_id": "123",
  "googleads_id": "123",
  "product_feed_type": "xml",
  "product_url_feed": "https://test.xml",
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
  "label_campaign": "0"
}
```

Response

```text
200 OK
```

```json
{
  "analytics_solution": "ga3",
  "analytics_id": "123",
  "googleads_id": "123",
  "product_feed_type": "xml",
  "product_url_feed": "https://test.xml",
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
  "label_campaign": "0" 
}
```
