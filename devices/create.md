---
layout: default
title: Create Device
parent: Devices
nav_order: 2
---

# Create Device

Create one or more show links.

### Request

```
POST https://studio.streamally.live/api/user/register
```

#### Parameters

| Parameter | Description |
|:-----|:-----|
| api_token * | Authentication token |
| name * | Name of the person who will be using the show link |
| email * | Email of the person who will be using the show link |
| show_id * | The UUID of the show for which this device should be registered |
| phone | Phone number of the person who will be using the show link |
| devices | Number of devices that should be created for the user (defaults to 1). |
| notify | Send value of `1` if StreamAlly should send the user their show links by email and/or SMS |
| unique_id | A unique identifier for the device or devices. If provided, this identifier will make sure subsequent requests with the same identifier do not produce additional links |

#### \* Required fields denoted by asterisk

### 200 Response

```
{
    "success": true,
    "user": {
        "name": "Dwight S",
        "email": "test@example.net",
        "phone": ""
    },
    "links": [
        "https://studio.streamally.live/show/view/b9b521c3-e3a2-475f-b2b9-1d02a3cfea64?token=sxHOrZiwP1bXPbVjtqhEyAsyR5uqmZCH"
    ]
}
```
