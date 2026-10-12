# Implement UI Policy in ServiceNow — Incident Management

A ServiceNow project focused on configuring a UI Policy for Incident records. Supporting Client Scripts are included to demonstrate related form behavior and validation.

## Main Project
**Primary configuration:** `High Impact Control` UI Policy  
**Table:** Incident  
**Condition:** Impact is `1 - High`  
**UI Policy Action:** Assignment group — Mandatory = True  
**Reverse if false:** Enabled

When Impact is High, Assignment group becomes mandatory. When the condition becomes false, the UI Policy reverses the mandatory behavior.

## Supporting Client Scripts
1. `Auto set urgency for high impact` — sets Urgency to High when Impact changes to High.
2. `Prevent save if Assigned To missing` — blocks form submission when Impact is High and Assigned to is empty.
3. `Prevent state change via list edit` — rejects direct State list edits.

## Repository Contents
- `01-Brainstorming-and-Ideation.md`
- `02-Requirement-Analysis.md`
- `03-Project-Design.md`
- `04-Project-Planning.md`
- `05-Project-Development.md`
- `06-Project-Testing.md`
- `07-Project-Documentation.md`
- `08-Project-Demonstration.md`

## Platform
ServiceNow Incident Management. This project is configured directly in ServiceNow; it does not require a separate local application stack.

## Team
## Team Members

| Name | Role |
|---|---|
| ARUNKRISHNA R S | Team Leader / Developer |
| KANNA K S | Administrator / Developer |
| KAVINRAJ T S | Administrator / Developer |
| RAKSHITH K | Tester |

## Before Submission
- Add screenshots from your ServiceNow instance.
- Record actual test outcomes in Phase 6.
- Add your public GitHub URL and public Google Drive demo URL in Phase 8.
- Do not commit passwords, session tokens, or other secrets.

## Limitations
The urgency script only sets Urgency to High when Impact becomes High; it does not reset Urgency when Impact changes away from High. The State list-edit script is client-side only and is not a server-side security control.
