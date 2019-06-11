---
category: Question
path: '/api/question/all'
title: 'Get all questions'
type: 'GET'

layout: nil
---

This method allows users to retrieve all questions.

### URL

`localhost:3000/api/question/all`


### Request

* Authentication is not required.

* Parameters are not required.

### Response

Returns an array of question objects.

```Status: 200 OK```
```
[
	{
		"category": "CSS Questions"
		"child_content": null
		"content": "What is CSS selector specificity and how does it work?"
		"id": 55
		"sort_order": 0
	},
	{ ... }
]
```

For error responses, see the [response status codes documentation](#response-status-codes).