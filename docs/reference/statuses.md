---
status: needs-review
primary: backend
---

# Statuses explained

Many records in AlignOne carry a **status** that tracks where they are in their lifecycle.
Statuses are managed lists — program staff can adjust the available options — so the live
list you see in the app is always the source of truth. Below are the standard values and
the few that drive how the system behaves.

## Family status

Tracks where a family is in the care journey.

- **Care Requested / Needs Vetting** — where a newly self-registered family starts. Staff
  must review and approve the family before it becomes active. *(The system enforces this
  gate, so this status matters.)*

Other common values include *Applicant*, *Active – Awaiting serving Church*,
*Active / Being served*, *On Hold*, and *Closed*.

## Volunteer status

Tracks where a volunteer is in their journey.

- **Prospect** — where a new or just-invited volunteer starts.

Other common values include *Equipped / Waiting*, *Serving*, *Taking a Break*,
*No Longer Serving*, and *Pending team placement*.

## Where statuses come from

Statuses are reference lists kept centrally and editable by staff, so treat the app's
current list as authoritative. Two values are special because the system acts on them:
**Care Requested / Needs Vetting** gates a family's approval, and **Prospect** is the
starting point for a new volunteer.
