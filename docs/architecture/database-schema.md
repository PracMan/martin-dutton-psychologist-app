# Martin Dutton Clinical Psychologist App

## Database Schema v1.0

### Document Information

| Item              | Value                 |
| ----------------- | --------------------- |
| Document          | Database Schema       |
| Version           | 1.0                   |
| Status            | Approved              |
| Database Platform | PostgreSQL (Supabase) |

---

# 1. Overview

This document defines the database structure for Version 1.0 of the Martin Dutton Clinical Psychologist App.

Version 1 focuses on:

* Announcements
* Push Notification Subscriptions
* Authentication

Blog content is sourced from the RSS feed and is not stored permanently.

---

# 2. Database Design Principles

The database must:

* Remain simple
* Minimize maintenance
* Support future growth
* Enforce security through RLS
* Maintain audit history

---

# 3. Entity Relationship Diagram

```text id="j6nh2o"
auth.users
    │
    │
    ▼
announcements

push_subscriptions
```

Version 1 intentionally contains few tables.

---

# 4. Table: announcements

Stores all published announcements.

## SQL Definition

```sql id="vtx3xt"
create table announcements (
  id uuid primary key default gen_random_uuid(),

  title text not null,

  message text not null,

  category text not null,

  is_active boolean default true,

  created_at timestamptz default now(),

  updated_at timestamptz default now(),

  created_by uuid references auth.users(id)
);
```

---

## Column Definitions

### id

Type:

UUID

Purpose:

Unique announcement identifier.

---

### title

Type:

TEXT

Purpose:

Announcement heading.

Example:

New Appointment Availability

---

### message

Type:

TEXT

Purpose:

Announcement body.

---

### category

Type:

TEXT

Allowed Values:

* general
* appointment
* blog

---

### is_active

Type:

BOOLEAN

Purpose:

Soft delete functionality.

---

### created_at

Type:

TIMESTAMP WITH TIME ZONE

Purpose:

Creation timestamp.

---

### updated_at

Type:

TIMESTAMP WITH TIME ZONE

Purpose:

Last update timestamp.

---

### created_by

Type:

UUID

Purpose:

Administrator who created record.

---

# 5. Table: push_subscriptions

Stores device notification subscriptions.

## SQL Definition

```sql id="r1h2el"
create table push_subscriptions (
  id uuid primary key default gen_random_uuid(),

  device_token text not null,

  platform text not null,

  active boolean default true,

  created_at timestamptz default now()
);
```

---

## Platform Values

Allowed:

```text id="3tq8ws"
android
ios
```

---

# 6. Indexes

## announcements

```sql id="7zhk31"
create index idx_announcements_created_at
on announcements(created_at desc);
```

---

```sql id="w9f6b0"
create index idx_announcements_active
on announcements(is_active);
```

---

## push_subscriptions

```sql id="4v4fpu"
create index idx_push_active
on push_subscriptions(active);
```

---

# 7. Row Level Security

## Enable RLS

```sql id="0h2m0x"
alter table announcements
enable row level security;
```

---

```sql id="g9v6mk"
alter table push_subscriptions
enable row level security;
```

---

# 8. Announcement Policies

## Public Read Access

```sql id="l0mxs8"
create policy "Public Read Announcements"

on announcements

for select

using (is_active = true);
```

---

## Admin Insert

```sql id="kh8g5q"
create policy "Admin Insert Announcements"

on announcements

for insert

to authenticated

with check (true);
```

---

## Admin Update

```sql id="2ywjjl"
create policy "Admin Update Announcements"

on announcements

for update

to authenticated

using (true);
```

---

## Admin Delete

```sql id="0v5skj"
create policy "Admin Delete Announcements"

on announcements

for delete

to authenticated

using (true);
```

---

# 9. Push Subscription Policies

## Public Insert

```sql id="srf4q7"
create policy "Public Register Device"

on push_subscriptions

for insert

with check (true);
```

---

## Public Update

```sql id="h5s7tq"
create policy "Public Update Device"

on push_subscriptions

for update

using (true);
```

---

# 10. Triggers

## Update Timestamp

```sql id="pq3gmx"
create or replace function update_timestamp()
returns trigger as $$
begin
  new.updated_at = now();
  return new;
end;
$$ language plpgsql;
```

---

```sql id="a2phlm"
create trigger update_announcements_timestamp

before update

on announcements

for each row

execute function update_timestamp();
```

---

# 11. Seed Data

## Sample Announcement

```sql id="mcn44v"
insert into announcements (
 title,
 message,
 category
)

values (

'Welcome',

'Welcome to the Martin Dutton Clinical Psychologist App.',

'general'

);
```

---

# 12. Backup Strategy

Provider:

Supabase

---

Frequency:

Daily

---

Retention:

30 Days

---

# 13. Future Tables

Version 1.1

Potential additions:

### resources

Resource library.

---

### saved_articles

User saved content.

---

### notification_history

Delivery tracking.

---

# 14. Acceptance Criteria

Database is complete when:

* Tables created
* RLS enabled
* Policies active
* Indexes created
* Seed data inserted
* Authentication functioning

---

# Version History

## Version 1.0

Initial approved schema.

Status:

Ready for Development
