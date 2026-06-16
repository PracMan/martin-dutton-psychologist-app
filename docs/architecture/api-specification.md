# Martin Dutton Clinical Psychologist App

## API Specification v1.0

### Document Information

| Item     | Value              |
| -------- | ------------------ |
| Document | API Specification  |
| Version  | 1.0                |
| Status   | Approved           |
| API Type | REST API           |
| Backend  | Next.js API Routes |
| Database | Supabase           |

---

# 1. Overview

This document defines all API endpoints used by the Martin Dutton Clinical Psychologist App.

The API is responsible for:

* Retrieving announcements
* Creating announcements
* Managing push notification subscriptions
* Retrieving blog content
* Securing administrative functions

---

# 2. Base URL

Development:

```text
http://localhost:3000/api
```

Production:

```text
https://app.mjwdpsych.com/api
```

---

# 3. Authentication

## Public Endpoints

Authentication not required.

Examples:

* Get announcements
* Get blog articles

---

## Admin Endpoints

Authentication required.

Provider:

Supabase Auth

---

# 4. Announcements API

## Get All Announcements

### Endpoint

```http
GET /api/announcements
```

### Description

Returns all active announcements.

### Response

```json
[
  {
    "id": "uuid",
    "title": "New Appointment Availability",
    "message": "Additional evening appointments are now available.",
    "category": "appointment",
    "created_at": "2026-06-01T12:00:00Z"
  }
]
```

### Status Codes

| Code | Meaning      |
| ---- | ------------ |
| 200  | Success      |
| 500  | Server Error |

---

## Get Announcement By ID

### Endpoint

```http
GET /api/announcements/{id}
```

### Response

```json
{
  "id": "uuid",
  "title": "New Appointment Availability",
  "message": "Additional evening appointments are now available.",
  "category": "appointment"
}
```

### Status Codes

| Code | Meaning      |
| ---- | ------------ |
| 200  | Success      |
| 404  | Not Found    |
| 500  | Server Error |

---

# 5. Admin API

## Create Announcement

### Endpoint

```http
POST /api/admin/announcements
```

### Authentication

Required

### Request

```json
{
  "title": "New Appointment Availability",
  "message": "Additional evening appointments are now available.",
  "category": "appointment"
}
```

### Validation

Title:

* Required
* Max 120 characters

Message:

* Required
* Max 5000 characters

Category:

* general
* appointment
* blog

### Response

```json
{
  "success": true,
  "announcementId": "uuid"
}
```

### Status Codes

| Code | Meaning          |
| ---- | ---------------- |
| 201  | Created          |
| 400  | Validation Error |
| 401  | Unauthorized     |
| 500  | Server Error     |

---

## Delete Announcement

### Endpoint

```http
DELETE /api/admin/announcements/{id}
```

### Authentication

Required

### Response

```json
{
  "success": true
}
```

### Status Codes

| Code | Meaning      |
| ---- | ------------ |
| 200  | Deleted      |
| 401  | Unauthorized |
| 404  | Not Found    |

---

# 6. Blog API

## Get Blog Feed

### Endpoint

```http
GET /api/blog
```

### Source

https://mjwdpsych.com/blog-feed.xml

### Response

```json
[
  {
    "title": "Understanding Anxiety",
    "url": "https://mjwdpsych.com/example",
    "excerpt": "An introduction to anxiety...",
    "publishedAt": "2026-06-01"
  }
]
```

### Status Codes

| Code | Meaning          |
| ---- | ---------------- |
| 200  | Success          |
| 503  | Feed Unavailable |

---

# 7. Push Notification API

## Register Device

### Endpoint

```http
POST /api/push/register
```

### Request

```json
{
  "deviceToken": "token",
  "platform": "android"
}
```

### Response

```json
{
  "success": true
}
```

### Status Codes

| Code | Meaning         |
| ---- | --------------- |
| 201  | Registered      |
| 400  | Invalid Request |
| 500  | Server Error    |

---

## Disable Device

### Endpoint

```http
POST /api/push/unregister
```

### Request

```json
{
  "deviceToken": "token"
}
```

### Response

```json
{
  "success": true
}
```

---

# 8. Error Response Format

All API errors must follow:

```json
{
  "success": false,
  "message": "Human readable error",
  "code": "ERROR_CODE"
}
```

---

# 9. Rate Limiting

Public Endpoints:

100 requests per minute

Admin Endpoints:

20 requests per minute

---

# 10. Logging

Log:

* Failed authentication
* Announcement creation
* Announcement deletion
* RSS feed failures
* Notification failures

---

# 11. Acceptance Criteria

The API is complete when:

* Announcements can be retrieved
* Announcements can be created
* Blog feed can be read
* Devices can register
* Admin authentication is enforced
* Standard error handling is implemented

---

# Version History

## Version 1.0

Initial approved API specification.

Status:

Ready for Development
