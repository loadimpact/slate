# Authentication

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: <YourAuthorizationToken>"
```


```python
client = loadimpact.ApiTokenClient(api_token='YOUR_API_TOKEN_GOES_HERE')
```

Load Impact expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: Token <YourAuthorizationToken>`  

Make sure to replace `<YourAuthorizationToken>` with your authorization token.

