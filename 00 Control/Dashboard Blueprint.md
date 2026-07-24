---
title: "Dashboard Blueprint"
type: dashboard-design
status: active
owner: "ONIRIA Operations"
created: 2026-07-24
last_updated: 2026-07-24
confidence: high
privacy: internal
---

# Dashboard Blueprint

## What the Dashboard Should Look Like

The ONIRIA dashboard should feel like an operating control room for a 20-room luxury hotel: calm, dense, visual, and action-focused. It should not look like a marketing home page. The first screen should immediately answer what is happening today, what is at risk, and where the team must act.

## First Screen

Use a compact four-zone layout:

| Zone | What it shows | Why it matters |
|---|---|---|
| Today | arrivals, departures, in-house guests, VIPs, room readiness | Keeps the guest journey visible |
| Rooms | room status, housekeeping status, maintenance holds, inspection gaps | Turns Property and rooms into daily action |
| Alerts | safety issues, guest complaints, overdue Actions, missing critical information | Keeps risk visible |
| Lulu | suggested actions, escalations, missing evidence, SOP lookups | Makes the AI useful without hiding accountability |

## Main Sections

1. **Guest and Room Readiness** - arrivals, preferences, room preparation, open defects and related SOPs.
2. **Property Health** - rooms 01-20, public areas, building systems, room layouts, render references and inspection status.
3. **Operations and SOPs** - priority SOPs, opening/closing checklists, daily checklist status and service standards.
4. **Maintenance and Inventory** - open requests, preventive maintenance, equipment, warranties, suppliers, stock and reorder risk.
5. **People, Safety and Compliance** - duty manager, roles on shift, training gaps, safety controls, incidents and compliance evidence.
6. **Missing Information** - critical unknowns, owner, affected area, due date and escalation path.

## Visual Style

- Use status chips for room states: Ready, Cleaning, Inspecting, Out of Service, Maintenance Hold, TO CONFIRM.
- Use small tables for daily operations rather than large narrative blocks.
- Use room thumbnails only where they help identify room character or design intent.
- Use traffic-light severity for risk: Critical, High, Medium, Low.
- Keep links close to decisions: each alert should link to the room, SOP, asset, supplier, staff role or REFERENCE evidence.

## Dashboard Rules

- Every dashboard item needs an owner or next action.
- Every technical or compliance claim needs REFERENCE evidence.
- Lulu can summarize and suggest, but safety, legal, privacy, major spend and guest-impacting decisions require human approval.
- Anything uncertain must stay marked TO CONFIRM until supported by an approved REFERENCE.

## Recommended Obsidian Layout

- Left column: Start Here, Today, Missing Information.
- Middle column: Rooms, SOPs, Maintenance.
- Right column: Safety, People, Lulu Escalations.
- Footer: live REFERENCE links, quality checklist and build status.
