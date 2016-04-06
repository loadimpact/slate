# User Scenarios

User scenario defines what URLs or web pages will be requested by the simulated users during a load test. The best user scenarios are ones that mimic real user behavior.  

Property | Description
---------| -----------
id | 
project_id | Related project ID ('one-to-many' relation)  
name | User scenario name
script | User scenario script
lines | TODO
data_store_ids | Related data store IDs as an array
data_store_counter | TODO
last_validation_id | TODO
last_validated | TODO
last_validation_error | TODO
belongs_to_user | TODO
created | User scenario creation datetime
updated | User scenario last update datetime

Read more about [User Scenarios](http://support.loadimpact.com/knowledgebase/topics/118845-user-scenario) in LoadImpact knoledge base.

## Index by project

```shell
### curl
curl "https://api.loadimpact.com/v3/projects/99/user-scenarios \"
  -H "Authorization: Token <YourAuthorizationToken>"

### Using the loadimpact cli
loadimpact user-scenario list --project_id=99
```

```python
The python SDK for the V3 API is still in BETA.

import loadimpact
client = loadimpact.ApiTokenClient(api_token='YOUR_API_TOKEN_GOES_HERE')
project_id = 1

client.list_user_scenarios(project_id)

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

`GET projects/<project_id>/user-scenarios HTTP/1.1`  
`Content-Type: application/json`  
`Authorization: Token <YourAuthorizationToken>`

URL Parameter | Description
------------- | -----------
project_id | Related project ID

## Create

```shell
### curl
curl "https://api.staging.loadimpact.com/v3/user-scenarios" \
  -H "Authorization: Token <YourAuthorizationToken>" \
  -XPOST \
  -d 'project_id=99' \
  -d 'name=New User Scenario 2' \
  -d 'script=script'

### Using the loadimpact cli
loadimpact user-scenario create 'script name' /path/to/script.lua --project_id=1
```

```python
The python SDK for the V3 API is still in BETA.

import loadimpact
client = loadimpact.ApiTokenClient(api_token='YOUR_API_TOKEN_GOES_HERE')


load_script = """
local response = http.get("http://example.com')
log.info("Load time: "..response.total_load_time.."s")
client.sleep(5)
"""
user_scenario = client.create_user_scenario({
    'name': "My user scenario",
    'load_script': load_script,
    'project_id': project_id
})

```

```json
{
  "user_scenario": {
    "id": 73,
    "project_id": 99,
    "name": "New User Scenario 2",
    "lines": 1,
    "script": "script",
    "data_store_ids": [],
    "data_store_counter": 0,
    "last_validated": null,
    "last_validation_id": null,
    "last_validation_error": "",
    "belongs_to_user": true,
    "created": "2016-04-05T09:32:14.368734",
    "updated": "2016-04-05T09:32:14.368760"
  }
}
```

`POST /user-scenarios HTTP/1.1`  
`Content-Type: application/json`  
`Authorization: Token <YourAuthorizationToken>`

<aside class="notice">TODO Show only creatable</aside>

Parameter | Requirements
--------- | ------------
name | Required string
script | Required text
project_id | Required ID
data_store_ids | TODO
data_store_counter | TODO

## Read

```shell
### curl
curl "https://api.loadimpact.com/v3/user-scenarios/67" \
  -H "Authorization: Token <YourAuthorizationToken>"  

### Using the loadimpact cli
loadimpact user-scenario get 67
```

```python
The python SDK for the V3 API is still in BETA.

import loadimpact
client = loadimpact.ApiTokenClient(api_token='YOUR_API_TOKEN_GOES_HERE')
user_scenario_id = 1

client.get_user_scenarios(user_scenario_id)
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
`Content-Type: application/json`  
`Authorization: Token <YourAuthorizationToken>`

Parameter | Description
--------- | -----------
ID | The ID of the user scenario to retrieve

## Update

```shell
### curl
curl "https://api.loadimpact.com/v3/user-scenarios/67" \
  -H "Authorization: Token <YourAuthorizationToken>" \
  -XPATCH \
  -d 'name=New User Scenario 1'

### Using the loadimpact-cli
loadimpact user-scenario update 67 /path/to/script.lua
```

```python
The python SDK for the V3 API is still in BETA.

import loadimpact
client = loadimpact.ApiTokenClient(api_token='YOUR_API_TOKEN_GOES_HERE')
scenario_id = 1

load_script = """
local response = http.get("http://example.com')
log.info("Load time: "..response.total_load_time.."s")
client.sleep(5)
"""

userscenario = client.get_user_scenario(scenario_id)
userscenario.update({'script': load_script})

```

```json
{
  "user_scenario": {
    "id": 67,
    "project_id": 99,
    "name": "New User Scenario 1",
    "data_store_ids": [],
    "script": "\nhttp.page_start(\"Page 1\")\nhttp.request_batch({\n    {\"GET\", \"http://google.ru/\"},\n    {\"GET\", \"http://www.google.ru/\"},\n})\nhttp.request_batch({\n    {\"GET\", \"http://www.google.ru/images/branding/product/ico/googleg_lodp.ico\"},\n    {\"GET\", \"http://www.google.ru/images/icons/product/chrome-48.png\"},\n    {\"GET\", \"http://www.google.ru/textinputassistant/tia.png\"},\n    {\"GET\", \"http://www.google.ru/images/branding/googlelogo/1x/googlelogo_white_background_color_272x92dp.png\"},\n    {\"GET\", \"http://www.google.ru/images/nav_logo229.png\"},\n})\nhttp.page_end(\"Page 1\")\n\nclient.sleep(math.random(20, 40))",
    "lines": 16,
    "data_store_counter": 0,
    "last_validation_id": 155,
    "last_validated": "2016-01-21T15:04:39.380270",
    "last_validation_error": "",
    "belongs_to_user": true,
    "created": "2016-01-20T11:59:32.368377",
    "updated": "2016-04-05T08:01:41.755627"
  }
}
```

`PATCH /user-scenarios/<ID>`  
`Content-Type: application/json`  
`Authorization: Token <YourAuthorizationToken>`

`PUT /user-scenarios/<ID>`  
`Content-Type: application/json`  
`Authorization: Token <YourAuthorizationToken>`


URL Parameter | Description
--------- | -----------
ID | The ID of the user scenario to retrieve


<aside class="notice">TODO Show only updatable</aside>

Parameter | Requirements
--------- | ------------
project_id | TODO
name | TODO
script | TODO
lines | TODO
data_store_ids | TODO
data_store_counter | TODO
last_validation_id | TODO
last_validated | TODO
last_validation_error | TODO
belongs_to_user | TODO

## Delete

```shell
### curl
curl "https://api.loadimpact.com/v3/user-scenarios/67" \
  -H "Authorization: Token <YourAuthorizationToken>" \
  -XDELETE

### Using the loadimpact-cli
loadimpact user-scenario delete 67
```

```python
The python SDK for the V3 API is still in BETA.

import loadimpact
client = loadimpact.ApiTokenClient(api_token='YOUR_API_TOKEN_GOES_HERE')
scenario_id = 1


userscenario = client.get_user_scenario(scenario_id)
userscenario.delete()
```


`DELETE /user-scenarios/<ID>`  
`Content-Type: application/json`  
`Authorization: Token <YourAuthorizationToken>`

URL Parameter | Description
--------- | -----------
ID | The ID of the user scenario to delete
