---
title: Lulu Missing Information Alerts
type: ai-workflow
status: draft
owner: Saleh Haji Othman
created: 2026-07-24
last_updated: 2026-07-24
confidence: medium
privacy: internal
---

# Lulu Missing Information Alerts

## Purpose

This note defines how Lulu detects, records, requests, tracks, and escalates missing information.

Lulu must not guess important facts when required information is unavailable, unclear, outdated, incomplete, or conflicting.

## What Counts as Missing Information

Missing information includes:

- A required field is empty
- A document or record is unavailable
- Information is unclear
- Information is outdated
- Two trusted sources conflict
- Evidence is missing
- Approval has not been recorded
- A responsible person is not assigned
- A deadline is not provided
- A room, guest, supplier, staff member, task, asset, or system cannot be identified
- A required safety or compliance record is absent

## Detection Process

When Lulu detects missing information, it must:

1. Identify the missing item
2. Identify the affected workflow
3. Explain why the information is required
4. Assess urgency and risk
5. Identify the responsible person or source
6. Prepare a clear question
7. Record the request
8. Pause affected high-risk actions
9. Track the response deadline
10. Validate the information when received
11. Continue the original workflow
12. Record the final outcome

## Alert Levels

### Green: Routine Information Request

Use when the missing information does not create immediate operational risk.

Examples:

- Missing non-critical note metadata
- Missing review date
- Missing optional description
- Missing routine follow-up detail

Lulu should:

- Record the missing item
- Ask the responsible person
- Set a normal follow-up date
- Continue unaffected work

### Amber: Attention Required

Use when missing information may affect cost, time, guest service, staffing, procurement, maintenance, or room operations.

Examples:

- Supplier delivery date missing
- Task owner missing
- Room number missing from a maintenance request
- Staff shift confirmation missing
- Guest request deadline unclear
- Quotation terms incomplete

Lulu should:

- Notify the responsible person
- Explain the operational effect
- Set a response deadline
- Pause the affected action when necessary
- Escalate if no response is received

### Red: Urgent

Use when missing information affects safety, security, privacy, legal compliance, emergency response, major financial action, or serious guest impact.

Examples:

- Fire safety inspection record missing
- Emergency contact unavailable
- Guest identity cannot be verified for a sensitive action
- Approval missing for a major purchase
- Legal or licence record missing
- Security access authority unclear

Lulu must:

1. Stop the affected automated action
2. Notify the responsible manager immediately
3. Record the issue and evidence
4. Explain the possible impact
5. Request urgent confirmation
6. Track acknowledgement
7. Continue only after authorised instruction

## Required Alert Fields

Every missing-information alert should include:

```yaml
alert_id:
title:
status:
risk_level:
missing_information:
reason_required:
affected_workflow:
affected_record:
responsible_person:
requested_from:
date_identified:
response_deadline:
source:
confidence:
approval_required:
escalation_status:
resolution:
date_resolved:
Alert Statuses

Use these statuses:

Open
Request prepared
Request sent
Waiting for response
Reminder sent
Escalated
Information received
Validation required
Resolved
Cancelled
Archived
Question-Writing Rule

Every question should be:

Clear
Specific
Directed to the responsible person
Connected to the affected action
Limited to the information needed
Free from assumptions
Question Template
Please confirm [missing information] for [related record or activity].

This information is required because [reason].

The affected action is [action or workflow].

Please respond by [deadline].
Examples
Missing Room Number
Please confirm the room number for the reported air-conditioning problem.

This information is required to identify the correct unit and retrieve its maintenance history.

The maintenance assignment is paused until the room is confirmed.
Missing Supplier Delivery Date
Please confirm the expected delivery date for the quoted items.

This information is required to check whether the delivery matches the procurement schedule.

Please respond before the purchase recommendation is submitted for approval.
Missing Task Owner
Please confirm who is responsible for completing the room inspection.

The task cannot be tracked or escalated without an assigned owner.
Missing Approval
The purchase request does not include approval from the authorised manager.

Please provide the approval record before the order is sent.
Reminder Process

When no response is received:

Check whether the deadline has passed
Confirm the request was sent correctly
Send a reminder
Record the reminder
Reassess risk
Escalate when the delay affects operations
Do not repeatedly message people unnecessarily
Escalation Timing

Suggested timing:

Green: follow up within three working days
Amber: follow up within one working day
Red: notify immediately

Actual timing should follow the relevant SOP and urgency of the situation.

Information Validation

When information is received, Lulu must:

Confirm who provided it
Check whether the person is authorised
Check supporting evidence
Check whether the information is complete
Compare it with trusted records
Assign a confidence level
Update the affected record
Resume the paused workflow when safe
Close the alert with evidence
Duplicate Alert Rule

Before creating an alert, Lulu should check whether the same missing item is already being tracked.

When a duplicate exists:

Link the new request to the existing alert
Update the existing record
Avoid sending duplicate messages
Preserve all related evidence
Dashboard Summary

The missing-information dashboard should show:

Total open alerts
Red alerts
Amber alerts
Overdue responses
Alerts by department
Alerts by responsible person
Recently resolved alerts
Workflows currently paused
Average response time
Privacy Rule

Missing-information alerts must not expose sensitive guest, staff, financial, security, or legal information to unauthorised users.

Only the minimum required information should be included in notifications.

Audit Rule

Lulu must record:

What information was missing
When it was detected
Who was contacted
Questions sent
Reminders sent
Escalations
Information received
Validation result
Workflow resumed
Final resolution
Quality Checks

Before closing an alert, confirm:

The missing information was received
The source is authorised
Evidence is available
Conflicts were resolved
Related records were updated
The paused workflow was reviewed
The responsible person was notified
The resolution was recorded