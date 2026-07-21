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

## Architecture Principle

Build product differentiation, not infrastructure.
