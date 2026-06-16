# Martin Dutton Clinical Psychologist App

## Backend & Supabase Specification v1.0

### Document Information

| Item             | Value                            |
| ---------------- | -------------------------------- |
| Document         | Backend & Supabase Specification |
| Version          | 1.0                              |
| Status           | Approved                         |
| Backend Platform | Supabase                         |
| Authentication   | Supabase Auth                    |
| Notifications    | Firebase Cloud Messaging         |

---

# 1. Overview

This document defines the backend architecture for the Martin Dutton Clinical Psychologist App.

The backend is responsible for:

* Authentication
* Announcement storage
* Push notification subscriptions
* Content delivery
* Security
* Administrative functions

---

# 2. Technology Stack

## Backend

Supabase

Services Used:

* PostgreSQL Database
* Authentication
* Row Level Security (RLS)
* Edge Functions (Future)

---

## Notifications

Firebase Cloud Messaging (FCM)

Used for:

* Push Notifications
* Device Registration

---

# 3. User Roles

## Public User

Permissions:

* View announcements
* View blog content
* Access contact information
* Access crisis support

Restrictions:

* No write access
* No administrative access

---

## Administrator

Permissions:

* Login
* Create announcements
* Edit announcements
* Delete announcements
* Send notifications

---

# 4. Database Schema

## Table: announcements

Stores published announcements.

| Column     | Type      | Required |
| ---------- | --------- | -------- |
| id         | UUID      | Yes      |
| title      | TEXT      | Yes      |
| message    | TEXT      | Yes      |
| category   | TEXT      | Yes      |
| is_active  | BOOLEAN   | Yes      |
| created_at | TIMESTAMP | Yes      |
| updated_at | TIMESTAMP | Yes      |
| created_by | UUID      | Yes      |

---

### Example Record

```json
{
  "title": "New Appointment Availability",
  "message": "Additional evening appointments are now available.",
  "category": "appointment",
  "is_active": true
}
```

---

## Table: push_subscriptions

Stores notification subscriptions.

| Column       | Type      |
| ------------ | --------- |
| id           | UUID      |
| device_token | TEXT      |
| platform     | TEXT      |
| active       | BOOLEAN   |
| created_at   | TIMESTAMP |

---

### Platform Values

* android
* ios

---

# 5. Authentication

Provider:

Supabase Auth

---

## Authentication Method

Email + Password

---

## Supported Users

Version 1:

Single Administrator

Example:

```text
admin@mjwdpsych.com
```

---

# 6. Row Level Security (RLS)

## announcements

Public:

SELECT

Allowed

---

Public:

INSERT

Denied

---

Public:

UPDATE

Denied

---

Public:

DELETE

Denied

---

Administrator:

Full Access

Allowed

---

## push_subscriptions

Public:

INSERT

Allowed

Purpose:

Register device

---

Public:

UPDATE

Allowed

Purpose:

Deactivate subscription

---

Public:

DELETE

Denied

---

Administrator:

Full Access

Allowed

---

# 7. Announcement Workflow

## Publish Announcement

Step 1

Administrator logs in.

---

Step 2

Administrator creates announcement.

---

Step 3

Announcement inserted into database.

---

Step 4

Announcement appears:

* Home Screen
* Announcement Archive

---

Step 5

Notification event triggered.

---

Step 6

Push notification delivered.

---

# 8. Notification Architecture

Provider:

Firebase Cloud Messaging

---

## Trigger

New Announcement Published

---

## Notification Title

Martin Dutton Clinical Psychologist

---

## Notification Message

New announcement available.

Tap to view.

---

## Deep Link

```text
/announcements/{id}
```

---

# 9. Blog Integration

Source:

https://mjwdpsych.com/blog-feed.xml

---

## Sync Frequency

Every 60 minutes

---

## Data Retrieved

* Title
* URL
* Excerpt
* Publish Date
* Featured Image

---

## Storage Strategy

Cached only.

No permanent storage required.

---

# 10. API Endpoints

## Public

### Get Announcements

```http
GET /api/announcements
```

---

### Get Announcement

```http
GET /api/announcements/{id}
```

---

### Get Blog Feed

```http
GET /api/blog
```

---

## Admin

### Create Announcement

```http
POST /api/admin/announcements
```

---

### Delete Announcement

```http
DELETE /api/admin/announcements/{id}
```

---

# 11. Environment Variables

Required:

```env
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=

SUPABASE_SERVICE_ROLE_KEY=

NEXT_PUBLIC_FIREBASE_API_KEY=
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=
NEXT_PUBLIC_FIREBASE_PROJECT_ID=
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=
NEXT_PUBLIC_FIREBASE_APP_ID=

RECOMED_BOOKING_URL=
```

---

# 12. Security Requirements

All Admin Routes:

Authentication Required

---

Protected Routes:

```text
/admin
/admin/dashboard
/admin/announcements/new
```

---

Public Access:

Read Only

---

# 13. Backup Strategy

Provider:

Supabase

---

Frequency:

Daily

---

Retention:

30 Days

---

# 14. Monitoring

Monitor:

* Authentication Failures
* Notification Failures
* Database Errors
* RSS Feed Errors

---

# 15. Acceptance Criteria

The backend is considered complete when:

* Admin can login
* Admin can create announcements
* Notifications are delivered
* RSS feed synchronizes
* Public users can view announcements
* Public users cannot modify data

---

# Version History

## Version 1.0

Initial approved backend specification.

Status:

Ready for Development
