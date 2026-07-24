title: Lulu Knowledge Structure and Agent Architecture
type: ai-architecture
status: draft
created: 2026-07-24
last_updated: 2026-07-24
confidence: medium
privacy: internal
---

# Lulu Knowledge Structure and Agent Architecture

## Purpose

This note explains how Lulu connects to the ONIRIA Brain, specialised AI agents, humans, tools, and hotel business systems.

The architecture should allow Lulu to retrieve reliable information, coordinate work, apply permissions, record actions, and escalate important issues.

# Main Architecture

Lulu operates as the central coordination agent.

```text
Humans
   │
   ▼
Communication Interfaces
   │
   ▼
Lulu Central Agent
   │
   ├── Knowledge Retrieval
   ├── Planning and Reasoning
   ├── Permission Checking
   ├── Workflow Management
   ├── Tool Selection
   ├── Action Verification
   └── Memory Updating
   │
   ├──────── Specialised AI Agents
   │
   ├──────── ONIRIA Brain
   │
   └──────── Hotel Business Systems
Main Components
1. Human Interface Layer

Humans may communicate with Lulu through:

Email
Slack
WhatsApp
Voice notes
Forms
Dashboards
Internal chat
Staff applications

The interface should capture:

Sender
Date and time
Request
Department
Urgency
Related guest, room, Action, supplier, or system
Attached evidence
2. Lulu Central Agent

Lulu is responsible for:

Understanding requests
Identifying the operational area
Retrieving relevant knowledge
Detecting missing information
Assessing risk and urgency
Checking permissions
Preparing a plan
Selecting approved tools
Coordinating specialised agents
Checking action results
Updating records
Reporting and escalating
3. ONIRIA Brain

The ONIRIA Brain is Lulu's main structured knowledge REFERENCE.

It contains:

Guest experience information
Rooms and property records
Operating procedures
Maintenance records
Supplier and inventory records
Staff and compliance information
Decisions
Actions
Risks
REFERENCEs and evidence
Governance rules
Templates
Archived records

Lulu should retrieve information using note links, metadata, tags, identifiers, and relationships.

Knowledge Areas
Guest Experience

Contains:

Guest journey
Guest requests
Complaints
Service recovery
Front-office procedures
Guest preferences
Privacy rules
Property and Rooms

Contains:

Property map
Floor information
Room records
Public areas
Spa areas
Equipment
Building systems
Inspection records
Operations and SOPs

Contains:

Standard operating procedures
Department workflows
Checklists
Responsibilities
Service standards
Emergency procedures
Maintenance and Inventory

Contains:

Equipment records
Fault reports
Maintenance history
Suppliers
Quotations
Inventory
Deliveries
Spare parts
Staff and Compliance

Contains:

Staff roles
Responsibilities
Training
Safety
Compliance
Access permissions
Schedules
Decisions, Risks, and Actions

Contains:

Decision records
Risk records
Action items
Deadlines
Owners
Dependencies
Completion evidence
Specialised AI Agents

Lulu may coordinate smaller agents with limited roles.

Guest Experience Agent

Responsibilities:

Classify guest requests
Prepare draft responses
Track service completion
Identify repeated complaints
Recommend service recovery

Restrictions:

Cannot approve refunds
Cannot change bookings without approval
Cannot access unrelated private data
Room and Property Agent

Responsibilities:

Retrieve room information
Connect rooms to equipment and systems
Support inspections
Identify missing property information

Restrictions:

Cannot change official room records without review
Cannot approve building modifications
Operations Agent

Responsibilities:

Retrieve SOPs
Guide routine workflows
Create checklists
Detect process gaps

Restrictions:

Cannot change approved SOPs independently
Cannot override safety procedures
Maintenance Agent

Responsibilities:

Classify faults
Retrieve maintenance history
Suggest priority
Identify technicians, parts, and suppliers
Track work orders

Restrictions:

Cannot close critical faults without verification
Cannot approve dangerous technical actions
Procurement and Inventory Agent

Responsibilities:

Compare quotations
Monitor stock
Track deliveries
Identify shortages
Prepare procurement recommendations

Restrictions:

Cannot approve purchases
Cannot approve suppliers
Cannot approve payments
Staff and Compliance Agent

Responsibilities:

Retrieve staff roles
Detect missing training
Support schedule planning
Track compliance records

Restrictions:

Cannot make disciplinary decisions
Cannot change staff schedules without approval
Cannot expose confidential staff information
Risk and Decision Agent

Responsibilities:

Create risk records
Analyse effects
Track decisions
Identify overdue approvals
Connect decisions to resulting Actions

Restrictions:

Cannot make final high-risk decisions
Cannot close major risks without evidence
AI-to-AI Communication

Specialised agents should communicate with Lulu using structured messages.

Required Message Fields
agent_id
message_id
date_time
request_type
operational_area
subject
related_record
REFERENCE
confidence
risk_level
recommended_action
approval_required
evidence
status
Example
agent_id: maintenance-agent
message_id: MAINT-2026-004
date_time: 2026-07-24 10:30
request_type: equipment-fault
operational_area: maintenance
subject: air-conditioning failure
related_record: Room 08
confidence: high
risk_level: amber
recommended_action: assign approved technician
approval_required: no
evidence: inspection report
status: pending action
Business-System Connections

Lulu may connect to approved systems through APIs or controlled integrations.

Property Management System

Used for:

Reservations
Room status
Check-in and check-out
Guest profiles
Stay information
Booking Engine

Used for:

Availability
Reservation requests
Booking details
Rate information
Customer Relationship Management System

Used for:

Guest communication
Preferences
Follow-up
Service history
Maintenance System

Used for:

Fault reports
Work orders
Inspection records
Maintenance history
Inventory System

Used for:

Stock levels
Item movement
Reorder alerts
Delivery records
Staff Scheduling System

Used for:

Shifts
Coverage
Availability
Approved schedule changes
Communication Systems

Used for:

Email
Slack
WhatsApp
Notifications
Internal messages
Tool-Use Process

Before using a tool, Lulu must:

Identify the required action
Confirm the REFERENCE information
Check user and system permissions
Assess risk
Request approval when required
Select the approved tool

After using a tool, Lulu must:

Confirm whether the action succeeded
Record the result
Record any error
Update the related record
Notify the responsible person
Schedule follow-up when required
Memory Structure

Lulu uses different forms of memory.

Working Memory

Contains information needed for the current request.

Examples:

Current user request
Retrieved notes
Temporary plan
Tool response
Operational Memory

Contains active hotel information.

Examples:

Open Actions
Active risks
Current guest requests
Open maintenance faults
Pending approvals
Long-Term Memory

Contains approved and reusable knowledge.

Examples:

SOPs
Room information
Staff roles
Supplier records
Decisions
Policies
Audit Memory

Contains records of important actions.

Examples:

Approval history
Tool actions
System changes
Escalations
Errors
Final outcomes
Retrieval Process

When Lulu receives a request, it should:

Identify key entities
Identify the operational area
Search relevant folders
Retrieve linked notes
Check metadata
Compare REFERENCE priority
Check freshness
identify conflicts
assign confidence
use only relevant information
Required Identifiers

Important records should use consistent identifiers.

Examples:

Action-001
DEC-001
RISK-001
SOP-001
ROOM-01
EQUIP-001
SUP-001
STAFF-001
GUEST-REQUEST-001
COMPLAINT-001
REFERENCE-001

Identifiers help Lulu connect records accurately.

Metadata Requirements

Important notes should include:

title:
type:
status:
owner:
created:
last_updated:
confidence:
privacy:
department:
related_records:
review_date:
Access Control

Lulu should use role-based access.

Examples:

Front-office staff may access guest-service information
Maintenance staff may access equipment and work-order information
Managers may access operational summaries
Finance staff may access approved financial records
General staff should not access restricted guest, staff, or financial data
Failure Handling

When a tool, agent, or business system fails, Lulu must:

Record the failure
Avoid claiming success
Preserve the request
Explain the effect
Suggest a safe alternative
Notify the responsible person
Retry only when safe and permitted
record the final result
Security Rules

Lulu and specialised agents must:

Use minimum necessary permissions
Protect credentials
Avoid exposing sensitive data
Log important actions
Validate tool inputs
Check tool outputs
Prevent duplicate actions
Avoid unauthorised system changes
Escalate suspicious activity
Architecture Quality Rules

The architecture should ensure:

Every agent has a defined role
Every agent has limited permissions
Every action has a responsible owner
Important actions are traceable
High-risk decisions remain human-controlled
Information comes from trusted REFERENCEs
System errors are visible
Privacy is protected
Records remain connected
Lulu can explain why an action was recommended