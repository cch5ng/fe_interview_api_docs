---
category: Test
path: '/api/test/new'
title: 'Initialize Test'
type: 'POST'

layout: nil
---

This method is triggered automatically on successful call to Post requirements for random questions. This method will create a new test.

### URL

`localhost:3000/api/test/new`


### Request

* Authentication is required. The JWT token is sent in the request body.

```
{
	"name": str,
	"questions":
		[ {}, {}, {}] array of question objects, automatically populated
	"time_total": int, milliseconds
	"status": str, 'initialized' by default
	"email": str,
	"date_taken": str,
	"token": str
}
```

### Response

Returns the resulting test id.

```Status: 200 OK```
```
{ "test_id": int }
```

For error responses, see the [response status codes documentation](#response-status-codes).