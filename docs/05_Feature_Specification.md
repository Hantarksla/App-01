# Feature Specification

## Overview

This document defines the product feature scope and priority.

## Priority Levels

- P0: Required for MVP
- P1: Important after validation
- P2: Future expansion

# P0 Features

## Account System

Requirements:
- Apple Sign In
- Email authentication
- Profile management
- Unique username / UID

## Goal Management

Users can:
- Create goals
- Edit goals
- Archive goals
- Build an unlimited stage tree (stages, sub-stages, recursive)
- Reorder nodes; numbering follows tree position (1, 1.1, 1.1.1)
- Define milestone nodes (one-time, optional deadline)
- Define recurring action nodes (daily habits)

## Check-in

Each active leaf node is checked in daily:

- Done (check): completed
- Not done (cross): recorded as missed
  - Breaks the streak
  - Shown as a gap in the heatmap

Users also record:
- Duration
- Notes (always private)
- Timestamp

Parent nodes aggregate child completion automatically
and can be manually confirmed once children complete.

## Progress Visualization

Includes:
- Daily status
- Weekly statistics
- Heatmap calendar

## Friends

Users can:
- Search by UID
- Send requests
- Accept requests
- View progress status

## Silent Interaction

Types:

Encourage:
- Positive feedback

Nudge:
- Reminder signal

Completion:
- Achievement feedback

# P1 Features

- Apple Watch quick check-in
- Competition mode
- AI weekly reports
- Advanced analytics
- Goal Globe

## Goal Globe

Publish:
- Any goal tree can be published to the Globe
  (opt-in; goals are private by default)
- Only the goal structure is shared;
  notes and reflections stay private

Discover:
- 3D globe visualizes published goals worldwide
- Filters: category, region, companion count

Adopt:
- Clone a public goal tree into your own goals
- The clone is fully editable and detached from the original
- A source link is kept for companion statistics

Companions:
- The creator receives a haptic notification on each adoption:
  "This goal has a new companion. You are not alone."
- Companion dashboard shows per companion:
  - Today status (done / not done / no check-in)
  - Current streak
  - Last active time
- Adopters who never checked in are highlighted
- Companions only see each other's check-in status
  (no notes, no private profile data)

Nudge:
- Tap a companion to send a haptic nudge
- Preset positive messages only, no free text
- Rate limit: one nudge per companion per day

# P2 Features

- Team challenges
- Enterprise accounts
- AI personal coach
