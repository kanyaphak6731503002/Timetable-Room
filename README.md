# Timetable-Room
# PRD — Timetable & Room (Team 04)

## Purpose
Create personal schedules and maintain section time/room assignments without conflicts.

## Scope
Screens: my timetable, room schedule, staff room editor. Entities: Meeting, Room, Timetable, Conflict. REST: `GET /timetables/me`, `GET /rooms`, `GET /rooms/{id}/schedule`, `POST /meetings`, `PATCH /meetings/{id}`, `POST /conflicts/check`, `DELETE /meetings/{id}`.

## Integrations
Consume Course Catalog sections and `enrollment.changed`; publish `schedule.changed` to Notification Hub and Data & Analytics. Only staff with Identity room-planning roles can edit meetings.

## AI and quality
AI proposes alternative slots; fallback applies overlap and capacity rules. Tests (minimum 7): personal schedule, room lookup, create, update, time clash, capacity clash, enrollment-event replay.
