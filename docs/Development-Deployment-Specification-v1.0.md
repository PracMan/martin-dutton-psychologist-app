# Martin Dutton Clinical Psychologist App

## Development & Deployment Specification v1.0

### Document Information

| Item          | Value                                  |
| ------------- | -------------------------------------- |
| Document      | Development & Deployment Specification |
| Version       | 1.0                                    |
| Status        | Approved                               |
| Frontend      | Next.js                                |
| Language      | TypeScript                             |
| Styling       | Tailwind CSS                           |
| Backend       | Supabase                               |
| Notifications | Firebase Cloud Messaging               |
| Hosting       | Vercel                                 |

---

# 1. Overview

This document defines the development architecture, deployment process, folder structure, hosting strategy, and production release workflow for the Martin Dutton Clinical Psychologist App.

---

# 2. Technology Stack

## Frontend

Framework:

Next.js 15+

Language:

TypeScript

Styling:

Tailwind CSS

Routing:

App Router

---

## Backend

Provider:

Supabase

Services:

* PostgreSQL
* Authentication
* Row Level Security
* Storage (Future)

---

## Notifications

Firebase Cloud Messaging (FCM)

Used for:

* Push notifications
* Device registration

---

## Hosting

Frontend:

Vercel

Backend:

Supabase Cloud

---

# 3. Repository Structure

```text
martin-dutton-psychologist-app/
│
├── docs/
├── public/
├── src/
├── tests/
│
├── README.md
├── package.json
├── tsconfig.json
├── next.config.ts
└── tailwind.config.ts
```

---

# 4. Source Structure

```text
src/
│
├── app/
│
├── components/
│
├── hooks/
│
├── lib/
│
├── services/
│
├── types/
│
└── styles/
```

---

# 5. App Directory Structure

```text
app/
│
├── page.tsx
│
├── blog/
│   ├── page.tsx
│   └── [slug]/
│
├── contact/
│
├── crisis-support/
│
├── announcements/
│   ├── page.tsx
│   └── [id]/
│
├── admin/
│   ├── page.tsx
│   ├── dashboard/
│   └── announcements/
│
└── api/
```

---

# 6. Component Architecture

## Shared Components

```text
components/
│
├── Layout/
├── Navigation/
├── Cards/
├── Buttons/
├── Forms/
├── Logo/
└── Notifications/
```

---

## Cards

Components:

* AnnouncementCard
* BlogCard
* ContactCard
* CrisisSupportCard

---

## Buttons

Components:

* PrimaryButton
* SecondaryButton
* IconButton

---

# 7. Services Layer

```text
services/
│
├── announcements.ts
├── blog.ts
├── notifications.ts
├── auth.ts
└── recomed.ts
```

Responsibilities:

* API calls
* Business logic
* Data transformation

---

# 8. Environment Configuration

Development:

```env
.env.local
```

Production:

Managed in Vercel.

---

Required Variables:

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

# 9. PWA Configuration

Requirements:

* Installable
* Offline capable
* Responsive
* Notification enabled

---

Manifest:

```json
{
  "name": "Martin Dutton Clinical Psychologist",
  "short_name": "Martin Dutton",
  "theme_color": "#2E74B5",
  "background_color": "#FCFCFA"
}
```

---

# 10. Required Assets

## App Icon

Sizes:

* 192x192
* 512x512

---

## Apple Touch Icon

Size:

* 180x180

---

## Splash Screen Logo

Format:

SVG

Background:

Transparent

---

# 11. Firebase Setup

Create:

Firebase Project

Name:

Martin Dutton App

---

Enable:

Cloud Messaging

---

Generate:

Firebase Web Configuration

---

Store:

Vercel Environment Variables

---

# 12. Supabase Setup

Create:

Project Name:

martin-dutton-app

---

Tables:

* announcements
* push_subscriptions

---

Enable:

Authentication

---

Create:

Admin User

---

# 13. Deployment Architecture

Production URL:

```text
https://app.mjwdpsych.com
```

---

Admin URL:

```text
https://app.mjwdpsych.com/admin
```

---

Hosting:

Vercel

---

DNS:

Subdomain:

app

Target:

Vercel

---

# 14. CI/CD Workflow

Trigger:

Push to main branch

---

Workflow:

1. Build
2. Run checks
3. Deploy to Vercel

---

Deployment:

Automatic

---

Rollback:

Via Vercel deployment history

---

# 15. Testing Requirements

## Devices

Android

iPhone

iPad

Desktop

---

## Browser Testing

Chrome

Safari

Samsung Internet

Edge

---

## Functional Testing

Announcements

Blog Feed

Contact Methods

Booking

Notifications

Authentication

---

# 16. Release Process

Step 1

Complete Sprint Development

---

Step 2

Run Testing

---

Step 3

Fix Defects

---

Step 4

Deploy Production Build

---

Step 5

Validate Production

---

Step 6

Launch

---

# 17. Maintenance

Monitor:

* RSS Feed Health
* Notification Delivery
* Authentication Failures
* Deployment Failures

---

Review Frequency:

Monthly

---

# 18. Acceptance Criteria

Deployment is complete when:

* App loads successfully
* PWA installs correctly
* RSS feed synchronizes
* Notifications function
* RecoMed link functions
* Admin can publish announcements
* Public users can access content

---

# Version History

## Version 1.0

Initial approved development and deployment specification.

Status:

Ready for Development
