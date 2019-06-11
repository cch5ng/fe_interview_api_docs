---
category: Test
path: '/api/test/detail'
title: 'Get test by Id'
type: 'GET'

layout: nil
---

This method allows users to retrieve a test by test Id.

### URL

`localhost:3000/api/test/detail`


### Request

* Authentication is required. The JWT token is sent in the request body.

* The test id is required (string).

```
{
	"id": str,
	"token": str,
}
```

### Response

Returns an test object.

```Status: 200 OK```
```
{
	"name": str,
	"date_taken": str, date-time stamp
	"time_total": int, milliseconds
	"time_remaining": int, milliseconds
	"status": str, (should show possible values)
	"questions": [
		{
			"needs_review": boolean or null,
			"status": str, (should show possible values)
			"sort_order": int,
			"response": str or null,
			"id": int,
			"content": str,
			"child_content": str or null,
			"category": str
		},
		{ ... }
	]
}
```

For error responses, see the [response status codes documentation](#response-status-codes).