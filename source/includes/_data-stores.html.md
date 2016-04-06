# Data Stores

Data stores are used to parameterize data in load scripts. You create a data store from a CSV file containing the data you want to use in your load scripts.

Property | Description
---------| -----------
id | Data store id
project_id | Related project ID ('one-to-many' relation)  
name | User scenario name
status | TODO
rows | TODO
converted | TODO
public_url | The public url of the data store
created | User scenario creation datetime
updated | User scenario last update datetime

Read more about [Data Stores](http://support.loadimpact.com/knowledgebase/articles/174258-how-do-i-use-parameterized-data) in LoadImpact knoledge base.

## Index by project

```shell
curl "https://api.loadimpact.com/v3/projects/99/data-stores" \
  -H "Authorization: Token <YourAuthorizationToken>"
```

```python
TODO
```

```json
{
  "data_stores": [
    {
      "id": 26,
      "project_id": 99,
      "name": "Sample Data Store",
      "public_url": "https://s3-eu-west-1.amazonaws.com/loadimpact-staging-datastores-public/26-72988677-abda-45dc-9f7c-1f1620364579.csv",
      "rows": 6,
      "status": 2,
      "converted": null,
      "belongs_to_user": true,
      "created": "2016-04-05T14:39:52.945691"
    }, {
      "id": 27,
      "project_id": 99,
      "name": "Sample Data Store 2",
      "public_url": "https://s3-eu-west-1.amazonaws.com/loadimpact-staging-datastores-public/26-72988677-abda-45dc-9f7c-1f1620364579.csv",
      "rows": 6,
      "status": 2,
      "converted": null,
      "belongs_to_user": true,
      "created": "2016-04-05T14:39:52.945691"
    }
  ],
  "meta": {
    "next": null,
    "prev": null,
    "count": 2
  }
}
```

`GET projects/<project_id>/data-stores HTTP/1.1`  
`Content-Type: application/json`  
`Authorization: Token <YourAuthorizationToken>`

URL Parameter | Description
------------- | -----------
project_id | Related project ID

## Read

```shell
curl "https://api.loadimpact.com/v3/data-stores/26" \
  -H "Authorization: Token <YourAuthorizationToken>"  
```

```python
TODO
```

```json
{
  "data_store": {
    "id": 26,
    "project_id": 99,
    "name": "Sample Data Store",
    "public_url": "https://s3-eu-west-1.amazonaws.com/loadimpact-staging-datastores-public/26-72988677-abda-45dc-9f7c-1f1620364579.csv",
    "rows": 6,
    "status": 2,
    "converted": null,
    "belongs_to_user": true,
    "created": "2016-04-05T14:39:52.945691"
  }
}
```

`GET /data-stores/<ID> HTTP/1.1`  
`Content-Type: application/json`  
`Authorization: Token <YourAuthorizationToken>`

Parameter | Description
--------- | -----------
ID | The ID of the data store to retrieve

## Delete

```shell
curl "https://api.loadimpact.com/v3/data-stores/67" \
  -H "Authorization: Token <YourAuthorizationToken>" \
  -XDELETE

```

```python
TODO
```

`DELETE /data-stores/<ID>`  
`Content-Type: application/json`  
`Authorization: Token <YourAuthorizationToken>`

URL Parameter | Description
--------- | -----------
ID | The ID of the data store to delete

