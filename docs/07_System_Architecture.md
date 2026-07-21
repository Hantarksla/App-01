# System Architecture

## Overview

The system uses managed services to reduce development complexity.

## Architecture

```
Flutter iOS App
        |
        |
Supabase Platform
        |
+----------------+
| Auth           |
| PostgreSQL     |
| Storage        |
| Realtime       |
| Edge Functions |
+----------------+
        |
Firebase Cloud Messaging
        |
Apple Push Notification
```

## Mobile

Framework:
- Flutter

Responsibilities:
- UI
- Local state
- User interaction
- Device integration

## Backend

Initial:
- Supabase
- Edge Functions

Future:
- FastAPI services

## External Services

Authentication:
- Supabase Auth

Notifications:
- Firebase Cloud Messaging

Subscriptions:
- RevenueCat

AI:
- Model Provider API

## Core Data Model

Goal tree (recursive, PostgreSQL):

goals
- id, user_id
- parent_goal_id (nullable; tree read via recursive CTE)
- node_type (root | milestone | action)
- title, order_index
- deadline (milestones), schedule (recurring actions)
- visibility (private | globe)
- source_goal_id (nullable; set when adopted from the Globe)

check_ins
- id, goal_id (leaf node), user_id, date
- status (done | missed)
- duration, note (private)

goal_adoptions
- id, source_goal_id, adopted_goal_id, adopter_user_id

nudges
- id, from_user_id, to_user_id, goal_id
- message_key (preset messages only)
- unique constraint enforces one nudge per pair per day

Row Level Security:
- Notes visible only to the owner
- Companions see check-in status only
  (today status, streak, last active time)

## Architecture Principle

Build product differentiation, not infrastructure.
