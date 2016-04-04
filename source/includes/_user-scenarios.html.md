# User Scenarios

<aside class="notice">Work in progress</aside>

User Scenario - TODO <Description What is it>

Property | Description
---------| -----------
id | 
project_id | The 'belongs to' related project ID 
name | The name of the user scenario
script | The user scenario script
lines | TODO
data_store_ids | The 'has many' related data store IDs (array) 
data_store_counter | TODO
last_validation_id | TODO
last_validated | TODO
last_validation_error | TODO
belongs_to_user | TODO
created |  
updated | 

## Index by project

```shell
curl "https://api.loadimpact.com/v3/projects/99/user-scenarios"
  -H "Authorization: Token <YourAuthorizationToken>"

loadimpact user-scenario list --project_id=99
```

```python
TODO
```

```java
TODO
```

```json
{
  "user_scenarios": [
    {
      "id": 67,
      "project_id": 99,
      "name": "Auto generated from google.ru",
      "lines": 16,
      "last_validation_error": "",
      "created": "2016-01-20T11:59:32.368377",
      "updated": "2016-01-21T15:04:39.380270",
      "data_store_ids": [],
      "data_store_counter": 0,
      "last_validated": "2016-01-21T15:04:39.380270",
      "last_validation_id": 155,
      "belongs_to_user": true
    },
    {
      "id": 54,
      "project_id": 99,
      "name": "Auto generated from yandex.ru",
      "lines": 15,
      "last_validation_error": "",
      "created": "2016-01-15T09:59:49.604362",
      "updated": "2016-01-15T09:59:49.604381",
      "data_store_ids": [],
      "data_store_counter": 0,
      "last_validated": null,
      "last_validation_id": null,
      "belongs_to_user": true
    }
  ],
  "meta": {
    "next": null,
    "prev": null,
    "count": 2
  }
}
```

`GET projects/ID/user-scenarios HTTP/1.1`  
`Authorization: Token <YourAuthorizationToken>`

URL Parameter | Description
--------- | -----------
ID | The ID of the project

## Create

```shell
TODO
```

```make
TODO
```

```python
TODO
```

```java
TODO
```

```json
{
  "user_scenario": {}
}
```

`POST /user-scenarios HTTP/1.1`  
`Authorization: Token <YourAuthorizationToken>`

Parameter | Requirements
--------- | -----------
project_id | The 'belongs to' related project ID 
name | The name of the user scenario
script | The user scenario script
lines | TODO
data_store_ids | The 'has many' related data store IDs (array) 
data_store_counter | TODO
last_validation_id | TODO
last_validated | TODO
last_validation_error | TODO
belongs_to_user | TODO

## Read

```shell
curl "https://api.loadimpact.com/v3/user-scenarios/67"
  -H "Authorization: Token <YourAuthorizationToken>"

loadimpact user-scenario list
```

```python
TODO
```

```java
TODO
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

`GET /user-scenarios/<ID> HTTP/1.1`  
`Authorization: Token <YourAuthorizationToken>`

Parameter | Description
--------- | -----------
ID | The ID of the user scenario to retrieve

## Update

```shell
TODO
```

```make
loadimpact user-scenario list
```

```python
TODO
```

```java
TODO
```

```json
{
  "belongs_to_user": true,
  "data_store_ids": [],
  "lines": 16,
  "name": "Auto generated from yandex.ru",
  "project_id": "3035261",
  "script": "\nhttp.page_start(\"Page 1\")\nhttp.request_batch({\n    {\"GET\", \"http://google.ru/\"},\n    {\"GET\", \"http://www.google.ru/\"},\n})\nhttp.request_batch({\n    {\"GET\", \"http://www.google.ru/images/branding/product/ico/googleg_lodp.ico\"},\n    {\"GET\", \"http://www.google.ru/images/icons/product/chrome-48.png\"},\n    {\"GET\", \"http://www.google.ru/textinputassistant/tia.png\"},\n    {\"GET\", \"http://www.google.ru/images/branding/googlelogo/1x/googlelogo_white_background_color_272x92dp.png\"},\n    {\"GET\", \"http://www.google.ru/images/nav_logo229.png\"},\n})\nhttp.page_end(\"Page 1\")\n\nclient.sleep(math.random(20, 40))"
}
```

`PATCH /user-scenarios/<ID>`  
`PUT /user-scenarios/<ID>`

URL Parameter | Description
--------- | -----------
ID | The ID of the user scenario to retrieve

Parameter | Requirements
--------- | ------------
project_id | The 'belongs to' related project ID 
name | The name of the user scenario
script | The user scenario script
lines | TODO
data_store_ids | The 'has many' related data store IDs (array) 
data_store_counter | TODO
last_validation_id | TODO
last_validated | TODO
last_validation_error | TODO
belongs_to_user | TODO

## Delete

```shell
TODO
```

```make
loadimpact user-scenario list
```

```python
TODO
```

```java
TODO
```

```json
TODO
```

