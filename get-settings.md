[service-shoppyz](../../../../README.md) / [API](../README.md) / [sttings](./README.md) / Get settings

# Get settings

Get dimensions and metrics names and types for settings.

```text
GET /settings
```

## Exemple

```text
GET /settings
```

Response

```text
200 Ok
```

```json
{
  "custom_rules_settings": [
    {
      "name": "brand",
      "type": "string"
    }
  ],
  "analytics_feed": [
    {
      "type": "GA4"
    }
  ],
  "product_feed": [
    {
      "connector": "url",
      "type": "xml"
    },
    {
      "connector": "url",
      "type": "txt"
    }
  ],
  "product_feed_mapping":[
    "id", "title","brand", "availability", "price", "image_link"
  ],
  "scoring_settings": [
    "sessions", "conversions"
  ]
}

```
