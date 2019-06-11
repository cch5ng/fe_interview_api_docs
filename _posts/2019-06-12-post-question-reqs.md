---
category: Question
path: '/api/question/random'
title: 'Post requirements for random questions'
type: 'POST'

layout: nil
---

This method allows users to save the number of questions by category to choose for a new test.

### URL

`localhost:3000/api/question/random`


### Request

* Authentication is required. The JWT token is sent in the request body.

* For each question category, an integer value shows the number of questions to select (randomly) in a new test.

```
{
	questionData: {
		"Coding Questions": int,
		"CSS Questions": int,
		"Fun Questions": int,
		"General Questions": int,
		"HTML Questions": int,
		"JavaScript Questions": int,
		"Network Questions": int,
		"Performance Questions": int,
		"Testing Questions": int,
	}, 
	token: string
}
```

### Response

Returns an array of arrays (of question objects).

```Status: 200 OK```
```
[
	[	{
			"id": int,
			"content": str,
			"child_content": str or null,
			"category": str,
			"sort_order": int
		},
		{},
		{}
	],
	[],
	[]
]
```

For error responses, see the [response status codes documentation](#response-status-codes).