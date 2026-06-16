# Martin Dutton Clinical Psychologist App

## UI Component Specification v1.0

### Document Information

| Item           | Value                      |
| -------------- | -------------------------- |
| Document       | UI Component Specification |
| Version        | 1.0                        |
| Status         | Approved                   |
| Design System  | Martin Dutton App UI       |
| Primary Colour | #2E74B5                    |

---

# 1. Design Principles

The application must communicate:

* Calmness
* Trust
* Professionalism
* Simplicity
* Accessibility

The application must avoid:

* Visual clutter
* Excessive animations
* Corporate dashboard styling
* Overwhelming colour palettes

---

# 2. Colour Palette

## Primary Brand Colour

Blue

```css
#2E74B5
```

Usage:

* Primary buttons
* Links
* Active navigation
* Icons
* Notification highlights

---

## Background Colour

Warm White

```css
#FCFCFA
```

Usage:

* Screen backgrounds

---

## Card Background

```css
#FFFFFF
```

Usage:

* Announcement cards
* Blog cards
* Contact cards

---

## Primary Text

```css
#333333
```

---

## Secondary Text

```css
#666666
```

---

## Border Colour

```css
#E6E6E6
```

---

# 3. Typography

## Font Family

Montserrat

Fallback:

```css
Arial, sans-serif
```

---

## Heading 1

Size:

```css
24px
```

Weight:

```css
600
```

Colour:

```css
#333333
```

---

## Heading 2

Size:

```css
20px
```

Weight:

```css
600
```

---

## Body Text

Size:

```css
16px
```

Weight:

```css
400
```

Line Height:

```css
1.6
```

---

## Small Text

Size:

```css
14px
```

Colour:

```css
#666666
```

---

# 4. Branding Components

## Primary Logo

Blue Semicolon

Used on:

* Splash Screen
* Home Screen
* Login Screen
* App Icon

---

## Secondary Logo

Heartbeat + Semicolon

Used on:

* Website
* Marketing material
* Documentation

Not used as the primary mobile app logo.

---

# 5. Buttons

## Primary Button

Background:

```css
#2E74B5
```

Text:

```css
#FFFFFF
```

Height:

```css
48px
```

Border Radius:

```css
12px
```

Examples:

* Log In
* Publish Announcement
* Book Appointment

---

## Secondary Button

Background:

```css
#FFFFFF
```

Border:

```css
1px solid #2E74B5
```

Text:

```css
#2E74B5
```

---

# 6. Cards

## Announcement Card

Contains:

* Title
* Summary
* Date

Border Radius:

```css
16px
```

Padding:

```css
16px
```

Shadow:

```css
0 2px 8px rgba(0,0,0,0.05)
```

---

## Blog Card

Contains:

* Featured Image
* Title
* Excerpt
* Date

Radius:

```css
16px
```

---

## Contact Card

Contains:

* Icon
* Contact Method
* Action

Radius:

```css
16px
```

---

# 7. Navigation

## Public Navigation

Bottom Navigation

Items:

* Home
* Blog
* Book
* Contact

---

## Active State

Colour:

```css
#2E74B5
```

---

## Inactive State

Colour:

```css
#999999
```

---

# 8. Home Screen Layout

Order:

1. Logo
2. Latest Announcement
3. Featured Blog Article
4. Quick Access Grid

---

## Quick Access Grid

Layout:

2 x 2

Items:

* Book Appointment
* Blog
* Contact Martin
* Crisis Support

---

# 9. Blog Screen

Components:

* Search Bar
* Featured Article
* Blog List

No categories

No filters

No saved articles

---

# 10. Article Reader

Components:

* Hero Image
* Title
* Date
* Article Content
* Share Button

No save button

---

# 11. Contact Screen

Actions:

* Call
* WhatsApp
* Email

No office hours

No location

---

# 12. Crisis Support Screen

Components:

* Emergency Banner
* Crisis Contact Cards

Services:

* Emergency Services
* SADAG
* Lifeline South Africa
* Childline South Africa

No self-help content

---

# 13. Announcement Archive

Components:

* Announcement Cards
* Date
* Summary

No search

No categories

No filtering

---

# 14. Admin Screens

## Login

* Semicolon Logo
* Email
* Password
* Forgot Password
* Log In

No navigation

---

## Dashboard

Components:

* Recent Announcements
* Create Announcement
* Logout

No analytics

No statistics

No scheduling

---

## New Announcement

Fields:

* Title
* Message
* Category

Categories:

* General
* Appointment
* Blog

Button:

* Publish Announcement

---

# 15. Accessibility

Minimum Touch Target:

```css
44px
```

Minimum Contrast:

WCAG AA

Requirements:

* Screen reader labels
* Keyboard accessibility
* Descriptive button text

---

# 16. Responsive Design

Supported Devices:

* Android Phones
* iPhones
* iPads
* Small Tablets

Admin Interface:

Desktop responsive

---

# 17. Acceptance Criteria

Every screen must:

* Use approved branding
* Use approved colour palette
* Use approved typography
* Use consistent spacing
* Maintain calm visual appearance
* Remain usable on small screens

---

# Version History

## Version 1.0

Initial approved UI specification.

Status:

Ready for Development
