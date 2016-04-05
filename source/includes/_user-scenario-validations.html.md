# User Scenario Validations

User scenario validations process represented by the states of the User Scenario Validation resource.  

Property | Description
---------| -----------
id | 
user_scenario_id | Related User Scenario ID ('one-to-many' relation)  
status | Status code
status_text | Status text
started | Started time
queued | Queued time
ended | Ended time

Read more about [User Scenario Validations](http://support.loadimpact.com/knowledgebase/articles/174261-what-does-the-validation-function-do) in LoadImpact knoledge base.

## Index by User Scenario
```shell
curl "https://api.loadimpact.com/v3/user-scenarios/67/validations \"
  -H "Authorization: Token <YourAuthorizationToken>"
```

```python
TODO
```

```java
TODO
```

```json
{
  "user_scenario_validations": [
    {
      "id": 166,
      "user_scenario_id": 67,
      "status": 0,
      "status_text": "Queued",
      "queued": "2016-04-05T11:01:31.689626",
      "started": null,
      "ended": null
    },
    {
      "id": 165,
      "user_scenario_id": 67,
      "status": 0,
      "status_text": "Queued",
      "queued": "2016-04-05T10:27:31.799720",
      "started": null,
      "ended": null
    }
  ],
  "meta": {
    "next": null,
    "prev": null,
    "count": 2
  }
}
```

`GET /user-scenarios/<user_scenario_id>/validations HTTP/1.1`  
`Content-Type: application/json`  
`Authorization: Token <YourAuthorizationToken>`

URL Parameter | Description
------------- | -----------
user_scenario_id | Related User Scenario ID

## Create

```shell
curl "https://api.staging.loadimpact.com/v3/validations" \
  -H "Authorization: Token <YourAuthorizationToken>" \
  -XPOST \
  -d 'user_scenario_id=67'

loadimpact user-scenario validate 67
```

```python
TODO
```

```java
TODO
```

```json
{
  "user_scenario_validation": {
    "id": 166,
    "user_scenario_id": 67,
    "status": 0,
    "status_text": "Queued",
    "started": null,
    "queued": "2016-04-05T11:01:31.689626",
    "ended": null
  }
}
```

`POST /validations HTTP/1.1`  
`Content-Type: application/json`  
`Authorization: Token <YourAuthorizationToken>`

Parameter | Requirements
--------- | ------------
user_scenario_id | Required related user scenario ID

## Read

```shell
curl "https://api.loadimpact.com/v3/validations/166" \
  -H "Authorization: Token <YourAuthorizationToken>"  
```

```python
TODO
```

```java
TODO
```

```json
{
  "user_scenario_validation": {
    "id": 166,
    "user_scenario_id": 67,
    "status": 0,
    "status_text": "Queued",
    "started": null,
    "queued": "2016-04-05T11:01:31.689626",
    "ended": null
  }
}
```

`GET /validations/<ID> HTTP/1.1`  
`Content-Type: application/json`  
`Authorization: Token <YourAuthorizationToken>`

Parameter | Description
--------- | -----------
ID | The ID of the user scenario validation to retrieve
