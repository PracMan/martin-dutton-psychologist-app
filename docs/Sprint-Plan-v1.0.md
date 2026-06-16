# Martin Dutton Clinical Psychologist App

## Sprint Plan v1.0

### Document Information

| Item     | Value                                   |
| -------- | --------------------------------------- |
| Document | Sprint Plan                             |
| Version  | 1.0                                     |
| Status   | Approved                                |
| Project  | Martin Dutton Clinical Psychologist App |

---

# 1. Overview

This document defines the phased development approach for the application.

Each sprint delivers a complete and testable set of functionality.

The objective is to reduce risk and ensure incremental progress toward production launch.

---

# 2. Sprint Structure

| Sprint   | Focus                       |
| -------- | --------------------------- |
| Sprint 1 | Foundation & Infrastructure |
| Sprint 2 | Public App Screens          |
| Sprint 3 | Blog & Announcement System  |
| Sprint 4 | Admin Portal                |
| Sprint 5 | Push Notifications          |
| Sprint 6 | Testing & Production Launch |

---

# Sprint 1

## Foundation & Infrastructure

### Objective

Establish the development environment and project architecture.

---

## Tasks

### Repository Setup

* Create GitHub Repository
* Configure Branch Structure
* Create Documentation Structure

---

### Frontend Setup

* Create Next.js Project
* Configure TypeScript
* Configure Tailwind CSS
* Configure ESLint

---

### PWA Setup

* Configure Manifest
* Configure Service Worker
* Configure Offline Support
* Configure Install Prompt

---

### Backend Setup

* Create Supabase Project
* Configure Authentication
* Create Database Tables
* Configure RLS Policies

---

### Firebase Setup

* Create Firebase Project
* Enable Cloud Messaging
* Generate Keys

---

### Hosting Setup

* Create Vercel Project
* Connect GitHub Repository
* Configure Environment Variables

---

## Deliverables

* Running Application
* Development Environment
* PWA Foundation
* Database Foundation

---

## Exit Criteria

* Application Deploys
* Supabase Connected
* Firebase Connected
* Vercel Deployments Working

---

# Sprint 2

## Public App Screens

### Objective

Build all public-facing screens.

---

## Screens

### Splash Screen

* Logo
* Branding
* Startup Experience

---

### Home Screen

* Latest Announcement
* Featured Blog
* Quick Actions

---

### Blog Screen

* Search
* Featured Article
* Article Listing

---

### Article Reader

* Content Display
* Share Function

---

### Contact Screen

* Phone
* WhatsApp
* Email

---

### Crisis Support

* Emergency Contacts
* SADAG
* Lifeline
* Childline

---

## Deliverables

Fully navigable public application.

---

## Exit Criteria

All public screens functional.

---

# Sprint 3

## Blog & Announcement System

### Objective

Connect dynamic content.

---

## Blog Integration

Source:

https://mjwdpsych.com/blog-feed.xml

---

### Tasks

* RSS Parsing
* Article Mapping
* Featured Article Logic
* Blog Cache

---

## Announcement System

### Tasks

* Announcement Archive
* Announcement Detail Screen
* Home Screen Integration

---

## Deliverables

Dynamic blog and announcement content.

---

## Exit Criteria

RSS feed updates successfully.

---

# Sprint 4

## Admin Portal

### Objective

Allow Martin to manage announcements.

---

## Features

### Login

* Email
* Password

---

### Dashboard

* Recent Announcements
* New Announcement

---

### Announcement Form

* Title
* Message
* Category

---

### Logout

* Session Management

---

## Deliverables

Fully functional admin portal.

---

## Exit Criteria

Admin can publish announcements.

---

# Sprint 5

## Push Notifications

### Objective

Deliver announcements directly to users.

---

## Tasks

### Device Registration

* Android
* iPhone

---

### Notification Service

* Firebase Integration
* Notification Delivery

---

### Deep Linking

Notification

↓

Announcement Detail

---

## Deliverables

Working push notification system.

---

## Exit Criteria

Notifications successfully delivered.

---

# Sprint 6

## Testing & Launch

### Objective

Prepare production release.

---

## Functional Testing

* Blog
* Contact
* Booking
* Announcements
* Notifications

---

## Device Testing

### Android

* Chrome
* Samsung Internet

---

### iPhone

* Safari

---

### Tablet

* iPad

---

## Production Tasks

### DNS

Configure:

app.mjwdpsych.com

---

### SSL

Verify HTTPS

---

### Monitoring

* Error Monitoring
* Notification Monitoring
* RSS Monitoring

---

## Deliverables

Production-ready application.

---

## Exit Criteria

Application passes all testing.

---

# 3. Post Launch Roadmap

## Version 1.1

Potential Features

* Resources Section
* Saved Articles
* Enhanced Analytics

---

## Version 2.0

Potential Features

* Patient Accounts
* Secure Messaging
* Appointment History

---

# 4. Success Metrics

The project is successful when:

* Users can install the app
* Users receive notifications
* Blog content synchronizes automatically
* Appointments can be booked via RecoMed
* Martin can publish announcements
* Administration requires minimal effort

---

# Version History

## Version 1.0

Initial approved sprint plan.

Status:

Ready for Development
