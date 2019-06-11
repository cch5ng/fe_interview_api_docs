---
category: Test
path: '/api/test/updateQuestion'
title: 'Update Test Question'
type: 'POST'

layout: nil
---

This method allows users to save changes to a question (response/status) during a test session.

### URL

`localhost:3000/api/test/updateQuestion`


### Request

* Authentication is required. The JWT token is sent in the request body.

```
{
	"question_id": int,
	"question_status": str, (should show possible values)
	"response": str,
	"test_id": str,
	"token": str,
}
```

### Response

Returns the updated question id.

```Status: 200 OK```
```
int (questionId)
```

For error responses, see the [response status codes documentation](#response-status-codes).