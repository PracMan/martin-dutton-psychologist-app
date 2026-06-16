# Martin Dutton Clinical Psychologist App

## Deployment Architecture v1.0

### Document Information

| Item                 | Value                    |
| -------------------- | ------------------------ |
| Document             | Deployment Architecture  |
| Version              | 1.0                      |
| Status               | Approved                 |
| Hosting Platform     | Vercel                   |
| Backend Platform     | Supabase                 |
| Notification Service | Firebase Cloud Messaging |

---

# 1. Overview

This document defines how the application is deployed, hosted, secured, monitored and maintained in production.

The objective is to provide:

* High availability
* Low maintenance
* Secure administration
* Automated deployment
* Reliable notifications

---

# 2. Production Architecture

```text id="v3bc81"
Users
 │
 ▼
app.mjwdpsych.com
 │
 ▼
Vercel
 │
 ├── Next.js Frontend
 │
 ├── API Routes
 │
 ├── RSS Feed Integration
 │
 └── Firebase Messaging
 │
 ▼
Supabase
 │
 ├── Authentication
 ├── Announcements
 └── Push Subscriptions
 │
 ▼
Firebase Cloud Messaging
 │
 ▼
Android / iPhone Devices
```

---

# 3. Domain Architecture

## Main Website

```text id="v8qjzy"
https://mjwdpsych.com
```

Purpose:

Marketing website

Blog source

Practice information

---

## Application

```text id="4rjlwm"
https://app.mjwdpsych.com
```

Purpose:

Patient-facing application

---

## Admin Portal

```text id="1j9oqs"
https://app.mjwdpsych.com/admin
```

Purpose:

Announcement management

---

# 4. Hosting Architecture

## Frontend

Provider:

Vercel

Responsibilities:

* Next.js hosting
* Edge delivery
* SSL certificates
* Automatic deployments

---

## Backend

Provider:

Supabase

Responsibilities:

* Database
* Authentication
* Security
* Storage

---

## Notifications

Provider:

Firebase Cloud Messaging

Responsibilities:

* Device registration
* Notification delivery
* Deep linking

---

# 5. DNS Configuration

## Required Record

Subdomain:

```text id="6o1q4k"
app
```

Target:

Vercel

---

Example:

```dns id="1kpbpn"
app.mjwdpsych.com
```

---

# 6. SSL Configuration

Provider:

Vercel

Requirements:

* HTTPS enforced
* Automatic renewal
* Modern TLS support

---

# 7. Environment Management

## Development

```text id="cb6hmn"
.env.local
```

Local machine only.

---

## Production

Managed through:

Vercel Environment Variables

---

Required Variables:

```env id="m4q9cz"
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

# 8. CI/CD Pipeline

## Source Control

GitHub

Repository:

```text id="n3p7vk"
martin-dutton-psychologist-app
```

---

## Deployment Trigger

Push to:

```text id="rkpjlwm"
main
```

---

## Deployment Process

1. GitHub Push
2. Build Verification
3. Automated Deployment
4. SSL Validation
5. Production Release

---

# 9. Release Strategy

## Development

Feature branches:

```text id="sj4qq5"
feature/*
```

---

## Integration

```text id="l7h7gk"
develop
```

---

## Production

```text id="aqc8mr"
main
```

---

# 10. Backup Strategy

## Database

Provider:

Supabase

Frequency:

Daily

Retention:

30 Days

---

## Source Code

Provider:

GitHub

Continuous version history.

---

# 11. Monitoring

## Application Monitoring

Monitor:

* Page errors
* Failed API calls
* Build failures

---

## Database Monitoring

Monitor:

* Failed authentication
* Query performance
* Connection errors

---

## Notification Monitoring

Monitor:

* Failed notification delivery
* Registration failures

---

## RSS Feed Monitoring

Monitor:

* Feed availability
* Feed parsing failures

Source:

https://mjwdpsych.com/blog-feed.xml

---

# 12. Recovery Procedures

## Failed Deployment

Action:

Rollback via Vercel

---

## Failed Database Migration

Action:

Restore backup

---

## Notification Failure

Action:

Review Firebase logs

---

## RSS Failure

Action:

Display cached content

Log failure

Retry automatically

---

# 13. Security Architecture

Authentication:

Supabase Auth

---

Authorisation:

Row Level Security (RLS)

---

Admin Access:

Authenticated users only

---

Public Access:

Read-only

---

Secrets:

Stored in Vercel Environment Variables

Never committed to GitHub

---

# 14. Performance Targets

Initial Page Load:

Less than 2 seconds

---

Announcement Retrieval:

Less than 500ms

---

RSS Synchronisation:

Less than 5 seconds

---

Notification Delivery:

Less than 30 seconds

---

# 15. Production Readiness Checklist

Infrastructure:

* GitHub configured
* Vercel configured
* Supabase configured
* Firebase configured

---

Application:

* PWA installable
* RSS feed working
* RecoMed link working
* Notifications working

---

Security:

* SSL enabled
* Environment variables configured
* Authentication tested

---

Testing:

* Android tested
* iPhone tested
* Tablet tested

---

# 16. Acceptance Criteria

Deployment architecture is complete when:

* Application available at app.mjwdpsych.com
* Admin portal secured
* Database operational
* Notifications operational
* RSS feed synchronised
* Automated deployment functioning

---

# Version History

## Version 1.0

Initial approved deployment architecture.

Status:

Ready for Development
