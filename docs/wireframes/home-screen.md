# Martin Dutton Clinical Psychologist App

## Wireframe Specification

### Screen: Home Screen

Version: 1.0

Status: Approved

---

# Purpose

The Home Screen is the primary entry point into the application.

It provides immediate access to:

* Latest Announcement
* Featured Blog Article
* Appointment Booking
* Contact Options
* Crisis Support

The design should be calm, uncluttered and action-oriented.

---

# Layout Structure

```text
┌─────────────────────┐
│                     │
│     Semicolon       │
│       Logo          │
│                     │
├─────────────────────┤
│ Latest Announcement │
│                     │
│ Title               │
│ Summary             │
│ View All →          │
├─────────────────────┤
│ Featured Article    │
│                     │
│ Image               │
│ Title               │
│ Read Article →      │
├─────────────────────┤
│ Quick Actions       │
│                     │
│ Book   | Blog       │
│ Contact| Crisis     │
├─────────────────────┤
│ Home Blog Book Contact │
└─────────────────────┘
```

---

# Components

## Logo Section

### Component

Semicolon Logo

### Position

Top Centre

### Purpose

Brand recognition

### Action

None

---

# Latest Announcement Card

## Component

AnnouncementCard

### Data Source

Latest active announcement

### Fields

Title

Summary

Date

### Actions

Tap Card

↓

Announcement Detail

---

Tap View All

↓

Announcements Archive

---

# Featured Blog Card

## Component

FeaturedBlogCard

### Data Source

Latest RSS article

### Fields

Image

Title

Excerpt

Publication Date

### Actions

Tap Card

↓

Article Reader

---

# Quick Actions Grid

## Layout

2 × 2 Grid

### Card 1

Book Appointment

Action:

Open RecoMed

---

### Card 2

Blog

Action:

Open Blog List

---

### Card 3

Contact Martin

Action:

Open Contact Screen

---

### Card 4

Crisis Support

Action:

Open Crisis Support Screen

---

# Navigation Bar

## Type

Bottom Navigation

### Items

Home

Blog

Book

Contact

---

## Active State

Home

Colour:

#2E74B5

---

## Inactive State

#999999

---

# Empty States

## No Announcement

Display:

No announcements available.

---

## RSS Feed Unavailable

Display:

Latest articles currently unavailable.

---

# Loading States

Announcement Card

Skeleton Loader

---

Blog Card

Skeleton Loader

---

# Accessibility

Touch Targets

Minimum:

44px

---

All buttons require:

* Screen Reader Labels
* Keyboard Accessibility

---

# Responsive Behaviour

Supported:

* Android Phones
* iPhones
* Tablets

---

# Acceptance Criteria

User can:

* View latest announcement
* View latest blog article
* Access quick actions
* Navigate using bottom navigation

Home screen loads successfully on all supported devices.

---

# Navigation Map

Home

├── Announcement Detail

├── Announcement Archive

├── Article Reader

├── RecoMed

├── Contact

└── Crisis Support

---

Status:

Approved for Development
