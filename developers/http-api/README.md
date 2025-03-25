---
description: Use our REST API
icon: globe-pointer
---

# HTTP API

Welcome to the FetchFox REST API! This guide will help you get up and running quickly by covering authentication, basic request structure, and making your first API call.

### Base URL

### Authentication

To access the API, you need an API key. You can obtain your API key from your FetchFox account dashboard.

```url
https://fetchfox.ai/api/v2
```

Include your API key in the `Authorization` header of every request:

```bash
curl "https://fetchfox.ai/v2/example-endpoint" \
     -H "Authorization: Bearer YOUR_API_KEY"
```

### Making Your First API Call

Let's test your setup by making a simple request to fetch account details.

Request:

```bash
curl "https://fetchfox.ai/api/v2/user/me" \
     -H "Authorization: Bearer YOUR_API_KEY"
```

Example Response:

```json
{
  "id": "w62kk43ps3",
  "createdAt": "2025-01-09T19:56:17.164Z",
  "updatedAt": "2025-03-21 20:33:11.721346",
  "email": "johndoe@gmail.com",
  // ...
}

```
