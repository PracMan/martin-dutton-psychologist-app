# Martin Dutton Clinical Psychologist App

## Project Specification v1.0

### Document Information

| Item             | Value                                   |
| ---------------- | --------------------------------------- |
| Project          | Martin Dutton Clinical Psychologist App |
| Version          | 1.0                                     |
| Status           | Approved                                |
| Application Type | Progressive Web App (PWA)               |
| Target Platforms | Android, iPhone, iPad                   |
| Distribution     | Direct Install                          |
| Domain           | app.mjwdpsych.com                       |

---

# 1. Project Overview

The Martin Dutton Clinical Psychologist App is a Progressive Web App (PWA) designed to provide patients with convenient access to practice information, appointment booking, blog content, announcements, and crisis support resources.

The application will be installable on Android and iPhone devices without requiring publication through Google Play or the Apple App Store.

---

# 2. Project Goals

The application must:

* Provide a calm and professional digital experience.
* Improve communication with patients.
* Deliver practice announcements through push notifications.
* Provide easy access to blog content.
* Integrate with RecoMed for appointment booking.
* Provide direct contact options.
* Provide crisis support information.
* Minimize administrative overhead.

---

# 3. Target Users

## Primary Users

Patients of Martin Dutton Clinical Psychologist.

### User Goals

* Read practice announcements.
* Book appointments.
* Access blog articles.
* Contact Martin.
* Access crisis support information.

---

## Administrator

Martin Dutton.

### Administrator Goals

* Publish announcements.
* Notify users.
* Manage practice communications.

---

# 4. Project Scope

## Included Features

### Public Application

* Splash Screen
* Home Screen
* Blog List
* Article Reader
* Contact Screen
* Crisis Support Screen
* Announcement Archive
* Announcement Detail Screen

### Admin Application

* Login
* Dashboard
* New Announcement
* Logout

### Integrations

* RecoMed
* RSS Blog Feed
* Firebase Notifications

---

## Excluded Features

The following are intentionally excluded from Version 1:

* Patient Accounts
* Messaging
* Resources Library
* Mood Tracking
* Journaling
* Appointment Management
* Scheduling Announcements
* Saved Articles
* User Profiles
* Online Payments

---

# 5. Branding

## Primary Brand Element

Blue Semicolon

## Secondary Brand Element

Heartbeat Graphic

## Primary Colour

#2E74B5

## Design Style

* Minimalist
* Calm
* Professional
* Mobile-first

---

# 6. Public Screens

## Splash Screen

Purpose:

Display application branding during startup.

Content:

* Semicolon logo
* Martin Dutton
* Clinical Psychologist

---

## Home Screen

Content:

* Latest Announcement
* Featured Blog Article
* Quick Access Buttons

Quick Access:

* Book Appointment
* Blog
* Contact Martin
* Crisis Support

Navigation:

* Home
* Blog
* Book
* Contact

---

## Blog List

Features:

* Search
* Featured Article
* Blog Listing

Data Source:

https://mjwdpsych.com/blog-feed.xml

---

## Article Reader

Features:

* Hero Image
* Article Content
* Share Button

---

## Contact Screen

Actions:

* Call
* WhatsApp
* Email

---

## Crisis Support

Provides access to verified South African crisis support services.

---

## Announcement Archive

Displays all announcements.

Sorted newest first.

---

## Announcement Detail

Displays:

* Title
* Date
* Message

Optional:

* Book Appointment button

---

# 7. Booking Integration

Provider:

RecoMed

Booking URL:

https://www.recomed.co.za/psychologist/cape-town/martin-dutton/14430/20362/

Behaviour:

Open RecoMed booking page in browser.

---

# 8. Notification System

Trigger:

Announcement Published

Behaviour:

1. Store announcement.
2. Send push notification.
3. Update Home Screen.
4. Update Announcement Archive.

Notification Title:

Martin Dutton Clinical Psychologist

Notification Body:

New announcement available.

---

# 9. Success Criteria

Patients can:

* Install the app.
* Read announcements.
* Read blog articles.
* Book appointments.
* Contact Martin.
* Access crisis support.

Administrator can:

* Login securely.
* Publish announcements.
* Send notifications.
* Manage announcements.

---

# 10. Version History

## Version 1.0

Initial approved specification.

Status:

Ready for Development
