---
title: 'Response status codes'

layout: nil
---

### Success

Successes differ from errors in that their body may not be a simple response object with a code and a message. The headers however are consistent across all calls:

* `GET`, `POST` returns `200 OK` on success

When [retrieving stuff](#get-stuff) for example:

```Status: 200 OK```
```
   [
      {"id":508,"content":"What is CSS selector specificity and how does it work?","child_content":null,"category":"CSS Questions","sort_order":0},

      {"id":509,"content":"What's the difference between \"resetting\" and \"normalizing\" CSS? Which would you choose, and why?","child_content":null,"category":"CSS Questions","sort_order":1},
   ]
```

### Error

Error responses are simply returning [standard HTTP error codes](http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html) along with some additional information:

* The error code is sent back as a status header,
* The body includes an object describing both the code and message (for debugging and/or display purposes),
