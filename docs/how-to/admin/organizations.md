---
status: needs-ui
primary: frontend
---

<!-- @backend verified: families are associated with a county; advocates are scoped to a
     serving church (distinct from a family's attending church). Churches and communities/
     families can be CSV-imported, with imports recorded in the audit log. -->

# Manage churches & counties

**Who this is for:** Program staff (Admins and Coordinators).
**When to use it:** When you set up or update the churches and counties your program works
with.
**Before you start:** You're signed in with staff access.

!!! info "Screenshots coming"
    These steps are described in words for now; annotated screenshots land once the screens
    are final.

## Why churches and counties matter

- **Churches** are how advocates are scoped: an advocate can see every family whose
  **serving church** is theirs. (A family's *serving* church — the one coordinating care —
  can differ from the church a family *attends*.)
- **Counties** group families and volunteers geographically; coordinators manage by county.

## Manage churches

1. Open **Churches**.  <!-- @frontend: confirm the nav label and where it lives -->
2. **Add** a church, or open an existing one to edit its details.
3. Save. Advocates assigned to that church will see the families it serves.

## Manage counties

1. Open **Counties**.  <!-- @frontend: confirm the nav label and where county management lives -->
2. Add or update a county as needed.
3. Save.

## Import churches in bulk

1. Open the **import** tool and download the **church template**.
   <!-- @frontend: confirm where import lives and the template download -->
2. Fill it in and upload. Every import is recorded in the **audit log**.

## Related

- [Manage families & people](families-and-people.md)
- [Manage volunteers & advocates](volunteers-and-advocates.md)
- [Roles & who sees what](../../concepts/roles-and-visibility.md)
