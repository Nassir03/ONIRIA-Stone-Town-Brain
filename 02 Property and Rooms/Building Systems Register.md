---
title: Building Systems Register
type: building-systems-register
status: draft
owner: Saleh Haji Othman
created: 2026-07-24
last_updated: 2026-07-24
confidence: medium
privacy: internal
task: 2
source: ONIRIA Project Hub Reference
---

# Building Systems Register

## Purpose

This register makes the hotel infrastructure machine-readable before walls close and before operations begin.

## System Map

| System | Operational Purpose | Connected Notes | Verification Required |
|---|---|---|---|
| Power | Lighting, outlets, equipment, guest comfort | [[Property Map]], [[Equipment Inventory]] | MEP drawings and site check |
| Plumbing | Bathrooms, spa, pools, bar, drainage | [[Spa Area]], [[Rooftop]], [[Room Inspection Structure]] | MEP drawings and pressure test |
| Wi-Fi | Guest connectivity and AI-native service | Room notes, [[Lulu Operational Workflows]] | Coverage survey |
| KNX | Lighting, climate, scenes, automation | Room notes, [[Lulu Knowledge Structure and Agent Architecture]] | KNX schedule |
| Sensors | Occupancy, comfort, safety, maintenance triggers | Room notes, [[Safety Dashboard]] | Privacy and placement approval |
| Air conditioning | Guest comfort and humidity control | Room notes, [[Preventive Maintenance Schedule]] | Model, capacity, controls |
| Speakers | Music and ambient experience | Room notes, [[Guest Journey Overview]] | Placement and volume zones |
| Smart locks | Guest access and security | Room notes, [[Security Procedures]] | Lock model and PMS integration |
| Lighting | Guest atmosphere and safety | Room notes, [[Emergency SOPs]] | Lighting plan and scene schedule |
| Fire safety | Life safety and legal compliance | [[Fire Safety Procedures]], [[Compliance Register]] | Approved fire plan |
| Security | Guest and property protection | [[Security Procedures]] | Approved security plan |

## Required Device Fields

Every fixed device should eventually include:

- Device ID
- Device type
- Brand and model
- Room or area
- Exact location
- Connected system
- Power source
- Network or bus address
- Supplier
- Installer
- Warranty
- Manual
- Maintenance requirement
- Guest impact if failed
- Safety impact if failed
- Status
- Source

## Critical Pre-Wall Closure Items

- Confirm KNX topology
- Confirm cable pathways
- Confirm sensor locations
- Confirm smart-lock power and network requirements
- Confirm Wi-Fi access point placement
- Confirm speaker wiring
- Confirm AC control integration
- Confirm pool and spa waterproofing interfaces

## Connected Maintenance Records

- [[Equipment Inventory]]
- [[Preventive Maintenance Schedule]]
- [[Warranty Records]]
- [[Maintenance Dashboard]]
