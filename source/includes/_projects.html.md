# Projects

Project is a context for managing tests, user scenarios, data stores and organization members. Every organization can have several projects.

Property | Description
---------| -----------
id | 
name | Project name
description | Project descrition
organization_id | Related organization ID ("one-to-many" relation)
user_scenario_counter | TODO
test_counter | TODO
data_store_counter | TODO
is_default | TODO
created | Project creation datetime
updated | Project last update datetime

Read more about [Projects](http://support.loadimpact.com/knowledgebase/articles/780522-projects) in LoadImpact knoledge base.

## Index by organization

```shell
curl "https://api.loadimpact.com/v3/organizations/117/projects" \
  -H "Authorization: Token <YourAuthorizationToken>"

loadimpact organization projects 117
```

```python
The python SDK for the V3 API is still in BETA.

import loadimpact
client = loadimpact.ApiTokenClient(api_token='YOUR_API_TOKEN_GOES_HERE')
organization_id = 1

client.list_organization_projects(organization_id)
```

```json
{
  "projects": [
    {
      "id": 152,
      "name": "My project 1",
      "description": "",
      "organization_id": 117,
      "created": "2016-03-04T11:25:22.888269",
      "updated": "2016-03-04T11:25:22.888292",
      "user_scenario_counter": 0,
      "test_counter": 0,
      "data_store_counter": 0,
      "is_default": true
    }, {
      "id": 153,
      "name": "My project 2",
      "description": "",
      "organization_id": 117,
      "created": "2016-03-04T11:25:22.888269",
      "updated": "2016-03-04T11:25:22.888292",
      "user_scenario_counter": 0,
      "test_counter": 0,
      "data_store_counter": 0,
      "is_default": true
    }
  ],
  "meta": {
    "next": null,
    "prev": null,
    "count": 2
  }
}
```

`GET organizations/<organization_id>/projects HTTP/1.1`  
`Content-Type: application/json`  
`Authorization: Token <YourAuthorizationToken>`

URL Parameter | Description
------------- | -----------
organization_id | Related organization ID

## Read

```shell
curl "https://api.loadimpact.com/v3/projects/152" \
  -H "Authorization: Token <YourAuthorizationToken>"
```

```python
This is not availble through the python SDK
```

```json
{
  "project": {
    "id": 152,
    "name": "My project 1",
    "description": "",
    "organization_id": 117,
    "created": "2016-03-04T11:25:22.888269",
    "updated": "2016-03-04T11:25:22.888292",
    "user_scenario_counter": 0,
    "test_counter": 0,
    "data_store_counter": 0,
    "is_default": true
  }
}
```

`GET /projects/<ID> HTTP/1.1`  
`Content-Type: application/json`  
`Authorization: Token <YourAuthorizationToken>`

Parameter | Description
--------- | -----------
ID | The ID of the project to retrieve


