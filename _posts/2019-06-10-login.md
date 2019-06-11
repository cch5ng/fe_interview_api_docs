---
category: Authentication
path: '/api/auth/login'
title: 'Login'
type: 'Post'

layout: nil
---

This method allows users to log in.

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

Sends back a JWT token.

```
	{
		"jwt": str, // authentication token
		"email": str,
	}
```

For errors responses, see the [response status codes documentation](#response-status-codes).