# Errors

The Pathwright API may return the following error codes:


Error Code | Meaning
---------- | -------
400 | Bad Request -- Missing or invalid parameter
401 | Unauthorized -- Your API key is wrong or missing
403 | Forbidden -- Your API key lacks the necessary privileges
404 | Not Found -- The requested object could not be found
405 | Method Not Allowed -- HTTP verb is not supported by this call
429 | Too Many Requests -- You have hit our rate limiting
500 | Internal Server Error -- We had a problem with our server. Try again later
503 | Service Unavailable -- We are temporarily offline. We should return soon