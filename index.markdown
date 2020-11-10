---
layout: page
title: "Introduction"
nav_order: 1
---

# Authentication

The StreamAlly API uses token-based requests for authentication. 
Requests made to the API must include an `api_token` parameter, either in the query string or as a form-data attribute. 
API Tokens should be kept private and not exposed through your application (example: do not use in AJAX calls).

API tokens can be acquired by reaching out to `tech@streamally.live`.

**Note:** Each API Token is assigned to a user from your organization. In order to avoid issues in service, please make sure to request that API tokens be reassigned before removing users from your account.

# Requests and Responses

All requests return JSON responses.

### Sample Request

Get information about the user that is associated with the API Token.

```
GET https://studio.streamally.live/api/user?api_token=988881adc9fc3655077dc2d4d757d480b5ea0e11
```

### Sample Response

```
{
    "name": "Michael S",
    "email": "mscott@dunder-mifflin.net",
    "phone": "19545551234",
    "moderator": false
}
```
