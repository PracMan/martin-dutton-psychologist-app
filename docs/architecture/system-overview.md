# Martin Dutton Clinical Psychologist App

## System Overview v1.0

### Document Information

| Item              | Value                             |
| ----------------- | --------------------------------- |
| Document          | System Overview                   |
| Version           | 1.0                               |
| Status            | Approved                          |
| Architecture Type | Progressive Web Application (PWA) |
| Hosting Platform  | Vercel                            |
| Backend Platform  | Supabase                          |

---

# 1. Purpose

This document provides a high-level overview of the application architecture and how the major systems interact.

The purpose is to give developers, administrators, and future maintainers a clear understanding of the complete application ecosystem.

---

# 2. System Architecture

The application consists of five primary systems:

1. Frontend Application
2. Supabase Backend
3. Firebase Notification Service
4. RSS Blog Integration
5. RecoMed Appointment Integration

---

# 3. High-Level Architecture

```text
User
 │
 ▼
PWA Frontend (Next.js)
 │
 ├── Supabase
 │     ├── Authentication
 │     ├── Announcements
 │     └── Push Subscriptions
 │
 ├── Firebase Cloud Messaging
 │     └── Push Notifications
 │
 ├── RSS Feed
 │     └── Blog Content
 │
 └── RecoMed
       └── Appointment Booking
```

---

# 4. Frontend Application

Technology:

* Next.js
* TypeScript
* Tailwind CSS

Responsibilities:

* User Interface
* Navigation
* PWA Installation
* API Communication
* Content Display

---

# 5. Backend Services

Provider:

Supabase

Responsibilities:

* Authentication
* Data Storage
* Security
* Administrative Features

---

# 6. Notifications

Provider:

Firebase Cloud Messaging (FCM)

Responsibilities:

* Device Registration
* Push Notification Delivery
* Deep Linking

Trigger:

Announcement Published

---

# 7. Blog Content

Source:

https://mjwdpsych.com/blog-feed.xml

Responsibilities:

* Provide blog content
* Supply featured article
* Supply article metadata

Refresh Frequency:

Every 60 minutes

---

# 8. Appointment Booking

Provider:

RecoMed

Booking URL:

https://www.recomed.co.za/psychologist/cape-town/martin-dutton/14430/20362/

Responsibilities:

* Appointment Scheduling
* Calendar Integration
* Healthbridge Synchronisation

---

# 9. User Types

## Public User

Permissions:

* Read announcements
* Read blog articles
* Contact Martin
* Access crisis support
* Book appointments

---

## Administrator

Permissions:

* Login
* Create announcements
* Publish notifications
* Manage announcements

---

# 10. Public Application Structure

Screens:

* Splash Screen
* Home Screen
* Blog List
* Article Reader
* Contact
* Crisis Support
* Announcement Archive
* Announcement Detail

---

# 11. Administrative Structure

Screens:

* Login
* Dashboard
* New Announcement

Access URL:

/admin

---

# 12. Data Flow

## Announcement Publishing

Admin

↓

Create Announcement

↓

Supabase Database

↓

Home Screen Updated

↓

Archive Updated

↓

Firebase Notification

↓

User Receives Notification

---

## Blog Synchronisation

RSS Feed

↓

Parser

↓

Application Cache

↓

Blog List

↓

Article Reader

---

# 13. Security Overview

Authentication:

Supabase Auth

Authorisation:

Row Level Security (RLS)

Public Access:

Read Only

Administrative Access:

Authenticated Only

---

# 14. Deployment Architecture

Frontend:

Vercel

Backend:

Supabase Cloud

Notifications:

Firebase Cloud Messaging

Domain:

app.mjwdpsych.com

---

# 15. Success Criteria

The architecture is successful when:

* Public users can access content
* Administrators can publish announcements
* Notifications are delivered
* Blog content synchronises automatically
* Appointment booking functions correctly

---

# Version History

## Version 1.0

Initial approved architecture overview.

Status:

Ready for Development
