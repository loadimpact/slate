# User Scenarios

## Get a Specific User Scenario

```ruby
```
```python
```
```shell
curl "https://api.loadimpact.com/v3/user-scenarios/67"
  -H "Authorization: Token Your-API-Token-Here"
```

```json
{
  "user_scenario": {
    "id": 67,
    "project_id": 99,
    "name": "Auto generated from google.ru",
    "script": "\nhttp.page_start(\"Page 1\")\nhttp.request_batch({\n    {\"GET\", \"http://google.ru/\"},\n    {\"GET\", \"http://www.google.ru/\"},\n})\nhttp.request_batch({\n    {\"GET\", \"http://www.google.ru/images/branding/product/ico/googleg_lodp.ico\"},\n    {\"GET\", \"http://www.google.ru/images/icons/product/chrome-48.png\"},\n    {\"GET\", \"http://www.google.ru/textinputassistant/tia.png\"},\n    {\"GET\", \"http://www.google.ru/images/branding/googlelogo/1x/googlelogo_white_background_color_272x92dp.png\"},\n    {\"GET\", \"http://www.google.ru/images/nav_logo229.png\"},\n})\nhttp.page_end(\"Page 1\")\n\nclient.sleep(math.random(20, 40))",
    "lines": 16,
    "data_store_ids": [],
    "data_store_counter": 0,
    "last_validation_id": 155,
    "last_validated": "2016-01-21T15:04:39.380270",
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
id | The ID of the user scenario to retrieve
project_id | The ID of the project user scenario belongs to
name | The name of the user scenario
script | The user scenario script
lines | TODO
data_store_ids | The IDS of the data stores user scenario has
data_store_counter | TODO
last_validation_id | TODO
last_validated | TODO
last_validation_error | TODO
belongs_to_user | TODO
created | The datetime user scenario created 
updated | The datetime user scenario updated last time
