[service-shoppyz](../../../../README.md) / [API](../README.md) / [campaign](./README.md) / Add a campaign

# Add a campaign

Add a campaign, starting a first scoring with basic score.

```text
POST /campaigns
```

## Body

| Name                               | Description                                     |
|------------------------------------|-------------------------------------------------|
| `user`                             | User doing the request.                         | 
| `campaign_name`                    | Name of the campaign, lowercase.                |
| `analytics_solution`               | Choice of Analytics version.                    |
| `analytics_id`                     | Analytics ID                                    |
| `googleads_id`                     | Google Ads ID                                   |
| `product_feed_type`                | Type of product feed                            |
| `product_url_feed`                 | URL of the feed                                 |
| `feed_mapping`                     | List name and name_in_feed to map product feed. |
| `label_campaign`                   | Label between 0 and 4 for the campaign.         |
| `users_emails`                     | List of emails to share the google sheet.       |

## Example

```text
POST /campaigns

{
  "user": {
    "id": 1,
    "workspaces": [5],
    "role": "customer"
  },
  "name": "test",
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
  "label_campaign": "0",
  "users_emails": ["solene.vinsot@eskimoz.fr"]
}
```

Response

```text
201 Created
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
