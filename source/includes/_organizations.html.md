# Organizations

Organization is a context for managing members, projects - which includes tests, scenarios and data stores - monitoring agents and integrations. Each organization can also have its own subscription plan.  

Property | Description
---------| -----------
id | Organization id
name | Organization name
description | Organization descrition
subscription_ids | Related subscription IDs as an array
load_zone_ids | Related load zones IDs as an array
is_personal | TODO
owner_id | Id of the user that is the owner of the organization
billing_address | Billing adress of the organization
billing_country | Billing country of the organization
billing_email | Billing email of the organization
vat_number | TODO
credits | Number of credits for the organization
can_get_data_retention | TODO
created | Organization creation datetime
updated | Organization last update datetime

Read more about [Organizations](http://support.loadimpact.com/knowledgebase/articles/780474-organizations) in LoadImpact knoledge base.

## Index

```shell

### curl
curl "https://api.loadimpact.com/v3/organizations" \
  -H "Authorization: Token <YourAuthorizationToken>"

### Using the loadimpact cli
loadimpact organization list
```

```python
The python SDK for the V3 API is still in BETA.

import loadimpact
client = loadimpact.ApiTokenClient(api_token='YOUR_API_TOKEN_GOES_HERE')

client.list_organizations()
```

```json
{
  "organizations": [
    {
      "id": 117,
      "name": "org-2",
      "description": "",
      "subscription_ids": [],
      "load_zone_ids": [1, 2, 3, 4, 5, 6, 7, 8, 11, 12, 13, 14, 15, 19, 20, 22, 23, 25, 26, 27, 28, 29, 30],
      "is_personal": false,
      "owner_id": 95,
      "billing_address": "",
      "billing_country": "US",
      "billing_email": "",
      "vat_number": "",
      "credits": 0,
      "created": "2016-03-04T11:25:22.795975",
      "updated": "2016-03-04T11:25:22.796000",
      "can_get_data_retention": false
    },
    {
      "id": 79,
      "name": "org-1",
      "description": "",
      "subscription_ids": [77, 147],
      "load_zone_ids": [1, 2, 3, 4, 5, 6, 7, 8, 11, 12, 13, 14, 15, 19, 20, 22, 23, 25, 26, 27, 28, 29, 30],
      "is_personal": true,
      "owner_id": 95,
      "billing_address": "",
      "billing_country": "SE",
      "billing_email": "",
      "vat_number": "",
      "credits": 0,
      "created": "2015-11-09T11:36:42.741733",
      "updated": "2016-03-30T12:38:00.694004",
      "can_get_data_retention": false
    }
  ],
  "meta": {
    "next": null,
    "prev": null,
    "count": 2
  }
}
```

`GET /organizations HTTP/1.1`  
`Content-Type: application/json`  
`Authorization: Token <YourAuthorizationToken>`

## Read

```shell
curl "https://api.loadimpact.com/v3/organizations/117" \
  -H "Authorization: Token <YourAuthorizationToken>"
```

```python
This feature is not implemented for the python SDK
```

```json
{
  "organization": {
      "id": 117,
      "name": "org-2",
      "description": "",
      "subscription_ids": [],
      "load_zone_ids": [1, 2, 3, 4, 5, 6, 7, 8, 11, 12, 13, 14, 15, 19, 20, 22, 23, 25, 26, 27, 28, 29, 30],
      "is_personal": false,
      "owner_id": 95,
      "billing_address": "",
      "billing_country": "US",
      "billing_email": "",
      "vat_number": "",
      "credits": 0,
      "created": "2016-03-04T11:25:22.795975",
      "updated": "2016-03-04T11:25:22.796000",
      "can_get_data_retention": false
  }
}
```

`GET /organizations/<ID> HTTP/1.1`  
`Content-Type: application/json`  
`Authorization: Token <YourAuthorizationToken>`

Parameter | Description
--------- | -----------
ID | The ID of the organization to retrieve

