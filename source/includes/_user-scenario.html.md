# User Scenarios

## Get a Specific User Scenario

```ruby
```
```python
```
```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

```json
{
  "user_scenario": {
    "id": 67,
    "project_id": 99,
    "data_store_ids": [],
    "name": "Auto generated from google.ru",
    "script": "\nhttp.page_start(\"Page 1\")\nhttp.request_batch({\n    {\"GET\", \"http://google.ru/\"},\n    {\"GET\", \"http://www.google.ru/\"},\n})\nhttp.request_batch({\n    {\"GET\", \"http://www.google.ru/images/branding/product/ico/googleg_lodp.ico\"},\n    {\"GET\", \"http://www.google.ru/images/icons/product/chrome-48.png\"},\n    {\"GET\", \"http://www.google.ru/textinputassistant/tia.png\"},\n    {\"GET\", \"http://www.google.ru/images/branding/googlelogo/1x/googlelogo_white_background_color_272x92dp.png\"},\n    {\"GET\", \"http://www.google.ru/images/nav_logo229.png\"},\n})\nhttp.page_end(\"Page 1\")\n\nclient.sleep(math.random(20, 40))",
    "lines": 16,
    "last_validated": "2016-01-21T15:04:39.380270",
    "data_store_counter": 0,
    "last_validation_id": 155,
    "last_validation_error": "",
    "belongs_to_user": true,
    "created": "2016-01-20T11:59:32.368377",
    "updated": "2016-01-21T15:04:39.380270"
  }
}
```

This endpoint retrieves a specific user scenario.

### HTTP Request

`GET https://api.loadimpact.com/v3/user-scenarios/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the user scenario to retrieve


