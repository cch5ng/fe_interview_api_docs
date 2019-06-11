---
category: Authentication
path: '/api/auth/register'
title: 'Registration'
type: 'Post'

layout: nil
---

This method allows users to register an account.

### Parameters

Send as JSON in request body.
Set request header with { "Content-Type": "application/json" }

```
	{ 
		email: str,
		password: str,
	}
```

### Response

Sends back a user id.

```
	{ userId: int }
```

For errors responses, see the [response status codes documentation](#response-status-codes).