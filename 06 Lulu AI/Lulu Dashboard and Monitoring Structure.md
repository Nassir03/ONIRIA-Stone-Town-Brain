---
title: Lulu Dashboard and Monitoring Structure
type: ai-dashboard
status: draft
created: 2026-07-24
last_updated: 2026-07-24
confidence: medium
privacy: internal
---

# Lulu Dashboard and Monitoring Structure

## Purpose

This note defines what managers and authorised staff should see on the Lulu operational dashboard.

The dashboard should provide a clear view of:

- Urgent issues
- Pending approvals
- Overdue Actions
- Guest complaints and requests
- Room and maintenance problems
- Supplier and inventory concerns
- Missing information
- Active risks
- System failures
- Lulu activity and performance

The dashboard should help people understand what requires attention, who is responsible, and what action should happen next.

# Dashboard Principles

The dashboard should:

- Show the most important information first
- Use simple labels
- Avoid exposing restricted information
- Show current status
- Show owners and deadlines
- Show risk and urgency
- Link each item to its REFERENCE record
- Distinguish confirmed information from unverified information
- Show when data was last updated
- Avoid duplicate alerts

# Main Dashboard Sections

## 1. Urgent Alerts

Shows all red-level issues requiring immediate attention.

Examples:

- Fire or electrical safety issue
- Serious guest complaint
- Security concern
- Privacy breach
- Critical equipment failure
- Missing emergency or compliance record
- Major operational breakdown

Each alert should show:

- Alert ID
- Title
- Risk level
- Location
- Responsible person
- Time identified
- Current status
- Required action
- Approval required
- Escalation status
- Linked evidence

## 2. Pending Approvals

Shows actions waiting for authorised human approval.

Examples:

- Booking changes
- Supplier selection
- Purchase orders
- Staff schedule changes
- Compensation
- Room availability changes
- Risk closure
- External communication

Each approval should show:

- Approval ID
- Proposed action
- Requested by
- Department
- Risk level
- Reason
- Evidence
- Approver
- Requested date
- Deadline
- Current status

## 3. Overdue Actions

Shows Actions that passed their due dates.

Each Action should show:

- Action ID
- Title
- Owner
- Department
- Priority
- Due date
- Days overdue
- Related record
- Current status
- Blocking issue
- Escalation level

## 4. Guest Requests and Complaints

Shows active guest-service issues.

Each item should show:

- Request or complaint ID
- Guest reference
- Room
- Category
- Priority
- Responsible department
- Time received
- Response deadline
- Current status
- Guest satisfaction status
- Approval required
- Escalation status

Sensitive guest information must only be visible to authorised users.

## 5. Rooms and Maintenance

Shows room faults, unavailable rooms, inspections, and equipment problems.

Each item should show:

- Room or asset
- Issue
- Risk level
- Reported time
- Responsible technician
- Work-order status
- Required parts
- Estimated completion
- Room availability
- Completion evidence
- Verification status

## 6. Suppliers and Inventory

Shows procurement and stock concerns.

Each item should show:

- Supplier or item
- Issue
- Quantity
- Current stock
- Reorder level
- Expected delivery
- Delay
- Responsible person
- Approval status
- Operational effect
- Next action

## 7. Missing Information

Shows all open missing-information alerts.

Each alert should show:

- Alert ID
- Missing item
- Affected workflow
- Risk level
- Responsible person
- Requested from
- Date requested
- Response deadline
- Current status
- Reminder status
- Escalation status

## 8. Active Risks

Shows open risks affecting the project or hotel.

Each risk should show:

- Risk ID
- Title
- Category
- Probability
- Impact
- Risk level
- Owner
- Preventive action
- Response action
- Review date
- Current status
- Escalation status

## 9. Decisions Required

Shows decisions waiting for owners or approvers.

Each decision should show:

- Decision ID
- Question
- Decision owner
- Options
- Evidence
- Risks
- Approval required
- Deadline
- Current status
- Related Actions

## 10. Staff and Coverage

Shows staffing issues that affect operations.

Each item should show:

- Department
- Shift
- Required staff
- Assigned staff
- Missing coverage
- Training requirement
- Conflict
- Responsible manager
- Approval status
- Next action

## 11. Compliance and Safety

Shows inspections, licences, training, and mandatory records.

Each item should show:

- Record or requirement
- Department
- Responsible person
- Due date
- Status
- Evidence
- Risk level
- Days remaining or overdue
- Escalation level

## 12. System and Tool Health

Shows the condition of connected systems and tools.

Examples:

- Property management system
- Booking engine
- Maintenance system
- Inventory system
- Staff scheduling system
- Communication systems
- Lulu integrations

Each system should show:

- System name
- Connection status
- Last successful check
- Last error
- Failed actions
- Affected workflows
- Responsible technical owner
- Recovery status

## 13. Lulu Activity

Shows important work completed by Lulu.

Examples:

- Questions answered
- Alerts created
- Actions created
- Reminders sent
- Approvals requested
- Escalations made
- Tool actions
- Failed actions
- Knowledge updates suggested

Each activity should show:

- Activity ID
- Date and time
- Action
- Reason
- REFERENCE
- Permission level
- Approver
- Tool used
- Result
- Evidence

# Dashboard Filters

Users should be able to filter by:

- Date
- Department
- Risk level
- Status
- Owner
- Room
- Supplier
- Guest-service category
- Action priority
- Approval status
- Escalation level
- Confidence level

# Dashboard Views

## Executive View

Designed for management.

Shows:

- Red alerts
- Main risks
- Decisions required
- Pending approvals
- Major delays
- Guest-impact issues
- Financial and compliance concerns
- Daily operational status

## Department View

Designed for department leads.

Shows:

- Department Actions
- Staff coverage
- Guest requests
- Maintenance issues
- Supplier concerns
- Missing information
- Approvals
- Risks

## Personal Work View

Designed for individual staff.

Shows:

- Assigned Actions
- Due dates
- Reminders
- Pending responses
- Approvals requested
- Escalations
- Completion evidence required

## Audit View

Designed for authorised reviewers.

Shows:

- Approval history
- Tool actions
- System changes
- Escalations
- Errors
- REFERENCE records
- Final outcomes

# Status Labels

Use these statuses consistently:

- Open
- Pending information
- Pending approval
- Approved
- In progress
- Blocked
- Completed
- Escalated
- Failed
- Cancelled
- Archived

# Risk Colours

Use:

- Green: Normal
- Amber: Attention required
- Red: Urgent

Do not use colour alone. Always show the written risk label.

# Dashboard Summary Cards

Suggested top-level cards:

- Red alerts
- Amber alerts
- Pending approvals
- Overdue Actions
- Open guest complaints
- Rooms unavailable
- Critical maintenance issues
- Supplier delays
- Missing-information alerts
- Active high risks
- System failures
- Compliance items overdue

# Daily Monitoring Process

At the start of each day, Lulu should:

1. Retrieve current operational information
2. Check red and amber alerts
3. Check overdue Actions
4. Check pending approvals
5. Check guest complaints
6. Check unavailable rooms
7. Check critical maintenance issues
8. Check supplier delays
9. Check staffing gaps
10. Check missing information
11. Check compliance deadlines
12. Check system failures
13. Prepare the daily dashboard summary
14. Notify authorised managers

# Alert Notification Rules

Lulu should notify:

- Red alerts immediately
- Amber alerts according to the workflow deadline
- Green items through routine summaries

Notifications should include:

- Situation
- Risk level
- Operational effect
- Responsible person
- Required action
- Deadline
- Approval required
- REFERENCE link

# Data Quality Rules

Dashboard information must:

- Come from trusted records
- Show last updated date
- Show confidence level
- Show responsible owner
- Link to the REFERENCE
- Avoid duplicate records
- Flag outdated information
- Flag conflicting information
- Exclude unauthorised sensitive data

# Performance Measures

The dashboard may track:

- Average response time
- Average Action completion time
- Number of overdue Actions
- Number of unresolved complaints
- Number of red alerts
- Approval waiting time
- Missing-information response time
- Maintenance resolution time
- Supplier delay frequency
- Tool success rate
- Tool failure rate
- Percentage of actions with complete audit records

# Dashboard Quality Checklist

Before publishing the dashboard, confirm:

- Urgent items appear first
- Owners are visible
- Deadlines are visible
- Risk levels are clear
- Approval requirements are clear
- Sensitive information is protected
- Every item links to a REFERENCE
- Data freshness is visible
- Duplicate alerts are removed
- Filters work correctly
- Failed tool actions are visible
- Audit records are available