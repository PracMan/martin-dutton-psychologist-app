# Martin Dutton Clinical Psychologist App

## User Flow Specification v1.0

### Document Information

| Item        | Value                                   |
| ----------- | --------------------------------------- |
| Document    | User Flow Specification                 |
| Version     | 1.0                                     |
| Status      | Approved                                |
| Application | Martin Dutton Clinical Psychologist App |
| Type        | Progressive Web App (PWA)               |

---

# 1. Purpose

This document defines the user journeys and interactions throughout the application.

The objective is to ensure that:

* Navigation is intuitive.
* Users can accomplish tasks quickly.
* Administrative actions are efficient.
* The application remains simple and focused.

---

# 2. User Types

## Public User

Patients and visitors who use the application.

Permissions:

* View content
* Read announcements
* Read blog articles
* Contact Martin
* Access crisis support
* Book appointments

---

## Administrator

Martin Dutton

Permissions:

* Login
* Create announcements
* Publish notifications
* Manage announcements

---

# 3. Application Entry Flow

## First Launch

User opens app.

↓

Splash Screen

↓

Home Screen

---

## Returning User

User opens installed app.

↓

Home Screen

---

# 4. Home Screen Journey

Home Screen contains:

* Latest Announcement
* Featured Blog Article
* Quick Actions

User selects:

### Option A

Book Appointment

↓

RecoMed

---

### Option B

Blog

↓

Blog List

---

### Option C

Contact Martin

↓

Contact Screen

---

### Option D

Crisis Support

↓

Crisis Support Screen

---

### Option E

Latest Announcement

↓

Announcement Detail

---

### Option F

View All Announcements

↓

Announcement Archive

---

# 5. Blog Journey

User taps:

Blog

↓

Blog List

---

User sees:

* Search Bar
* Featured Article
* Article List

---

User selects article

↓

Article Reader

---

User actions:

* Read Article
* Share Article

---

User returns

↓

Blog List

---

# 6. Booking Journey

User taps:

Book Appointment

↓

RecoMed Booking Page

↓

Appointment Booking

↓

Confirmation

---

User exits

↓

Return to App

---

# 7. Contact Journey

User taps:

Contact Martin

↓

Contact Screen

---

Available Actions:

### Call

Tap Phone Number

↓

Device Dialer

---

### WhatsApp

Tap WhatsApp

↓

WhatsApp Opens

---

### Email

Tap Email

↓

Email Application Opens

---

# 8. Crisis Support Journey

User taps:

Crisis Support

↓

Crisis Support Screen

---

User sees:

* Emergency Services
* SADAG
* Lifeline South Africa
* Childline South Africa

---

User taps service

↓

Phone Dialer Opens

---

# 9. Announcement Journey

## Home Screen

User taps latest announcement.

↓

Announcement Detail

---

OR

User taps:

View All

↓

Announcement Archive

---

User selects announcement

↓

Announcement Detail

---

# 10. Notification Journey

Announcement Published

↓

Push Notification Sent

↓

User taps notification

↓

Announcement Detail Screen

---

User may then:

* Return Home
* Book Appointment
* Read Other Announcements

---

# 11. Announcement Archive Journey

User opens:

Announcements Archive

↓

Announcement List

↓

Select Announcement

↓

Announcement Detail

↓

Back to Archive

---

# 12. Administrator Login Flow

Administrator visits:

/admin

↓

Login Screen

---

Enter:

* Email
* Password

↓

Submit

---

Authentication Successful

↓

Dashboard

---

Authentication Failed

↓

Error Message

↓

Retry

---

# 13. Administrator Dashboard Flow

Dashboard Displays:

* Recent Announcements
* New Announcement Button
* Logout

---

User selects:

Create Announcement

↓

Announcement Form

---

User selects:

Logout

↓

Session Ends

↓

Login Screen

---

# 14. Create Announcement Flow

Administrator opens:

New Announcement

↓

Enter:

* Title
* Message
* Category

---

Select:

Publish

↓

Announcement Saved

↓

Notification Triggered

↓

Dashboard

---

# 15. Error Flows

## RSS Feed Unavailable

Application displays:

Unable to load latest articles.

Please try again later.

---

## Notification Failure

Announcement still publishes.

Notification failure logged.

---

## Authentication Failure

Display:

Invalid email or password.

---

## Network Failure

Display:

Connection unavailable.

Please try again later.

---

# 16. Navigation Flow Diagram

Home

├── Blog

│   └── Article Reader

│

├── Book Appointment

│   └── RecoMed

│

├── Contact Martin

│

├── Crisis Support

│

└── Announcements

```
└── Announcement Detail
```

---

Admin

├── Login

│

└── Dashboard

```
├── New Announcement

└── Logout
```

---

# 17. User Experience Principles

The application should:

* Minimize taps
* Avoid unnecessary menus
* Present only relevant information
* Remain calm and professional
* Prioritize accessibility

---

# 18. Acceptance Criteria

Public Users Can:

* Read announcements
* Read blog content
* Contact Martin
* Access crisis support
* Book appointments

Administrator Can:

* Login
* Create announcements
* Publish notifications
* Logout

---

# Version History

## Version 1.0

Initial approved user flow specification.

Status:

Ready for Development
