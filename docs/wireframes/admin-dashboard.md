# Martin Dutton Clinical Psychologist App

## Wireframe Specification

### Screen: Admin Dashboard

Version: 1.0

Status: Approved

---

# Purpose

The Admin Dashboard provides a simple management interface for Martin to:

* View recent announcements
* Create new announcements
* Access announcement history
* Logout securely

The dashboard should remain intentionally lightweight and easy to use.

---

# Design Goals

The screen must feel:

* Professional
* Efficient
* Simple
* Uncluttered

Version 1 intentionally excludes analytics and reporting.

---

# Layout Structure

```text id="k3m7vx"
┌─────────────────────┐
│                     │
│     Dashboard       │
│                     │
├─────────────────────┤
│ New Announcement    │
├─────────────────────┤
│ Recent Announcements│
├─────────────────────┤
│ Announcement Card   │
├─────────────────────┤
│ Announcement Card   │
├─────────────────────┤
│ Announcement Card   │
├─────────────────────┤
│ Logout              │
└─────────────────────┘
```

---

# Components

## Screen Header

Title:

```text id="v6n4pj"
Dashboard
```

Position:

Top Centre

---

# New Announcement Button

## Component

PrimaryButton

Label:

```text id="w9q5mk"
New Announcement
```

---

## Action

Tap

↓

Open:

```text id="n8t3yr"
/admin/announcements/new
```

---

# Recent Announcements Section

## Purpose

Display recently published announcements.

---

## Data Source

Supabase

Table:

```text id="j7p4wa"
announcements
```

---

## Sorting

Newest First

---

# Announcement Card

## Fields

* Title
* Category
* Date Published

---

## Layout

```text id="m5v8zk"
Title

Category Badge

Published Date
```

---

## Actions

Tap Card

↓

Open Announcement Detail

(Future Enhancement)

---

# Category Badge

## General

Background:

```css id="q1x7br"
#EAF3FB
```

Text:

```css id="u4k9nh"
#2E74B5
```

---

## Appointment

Background:

```css id="p8m2yt"
#EEF7EE
```

Text:

```css id="g3w6rv"
#2F855A
```

---

## Blog

Background:

```css id="z5c1pk"
#FFF4E6
```

Text:

```css id="b2n8xj"
#DD6B20
```

---

# Logout Button

## Component

SecondaryButton

Label:

```text id="t7v4wy"
Logout
```

---

## Action

Tap

↓

End Session

↓

Redirect

```text id="r6m8qz"
/admin
```

---

# Empty States

## No Announcements

Display:

```text id="c3x5np"
No announcements published yet.
```

---

Button:

```text id="f8r2tk"
Create First Announcement
```

---

# Loading State

## Dashboard

Display:

* Skeleton Header
* Skeleton Button
* Skeleton Announcement Cards

Count:

3

---

# Error States

## Unable to Load Announcements

Display:

```text id="y4n7vm"
Unable to load announcements.
Please try again.
```

---

# Security Requirements

Authentication Required

---

Protected Route:

```text id="k9p3wa"
/admin/dashboard
```

---

Unauthenticated Users:

Redirect

↓

```text id="s2v6rk"
/admin
```

---

# Accessibility

Requirements:

* Screen reader support
* Accessible buttons
* Keyboard navigation
* Visible focus states

---

# Responsive Behaviour

Supported:

* Desktop
* Laptop
* Tablet
* Mobile

Primary target:

Desktop and Tablet

---

# Performance Requirements

Dashboard Load:

Less than 2 seconds

---

Announcement Retrieval:

Less than 500ms

---

# Acceptance Criteria

Administrator can:

* View recent announcements
* Create new announcements
* Logout securely

Dashboard loads correctly on all supported devices.

---

# Navigation Map

Dashboard

├── New Announcement

│   └── Create Announcement Screen

│

├── Recent Announcements

│

└── Logout

```
└── Login Screen
```

---

Status:

Approved for Development
