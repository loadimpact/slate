# Errors

<aside class="notice">Work in progress. Error Object needs to be described</aside>

Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request sucks
401 | Unauthorized -- Your API key is wrong
403 | Forbidden -- The resourse requested is protected and you don't have required permissions
404 | Not Found -- The specified resourse could not be found
405 | Method Not Allowed -- You tried to access a resourse with an invalid method
406 | Not Acceptable -- You requested a format that isn't json
429 | Too Many Requests -- You're requesting too many resourses! Slow down!
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarially offline for maintanance. Please try again later.
