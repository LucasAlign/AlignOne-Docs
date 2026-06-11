---
status: needs-ui
primary: frontend
---

<!-- @backend verified: a volunteer is scoped to ONE assigned family — assignment is what
     grants access. A volunteer can be marked Lead Volunteer for extra abilities within that
     one family. Advocates are scoped to their serving church. -->

# Manage volunteers & advocates

**Who this is for:** Program staff (Admins and Coordinators); advocates within their church.
**When to use it:** When you bring on a new volunteer or advocate, place them with a family,
or update their role or status.
**Before you start:** You're signed in with staff access, and the family you'll assign to
exists.

!!! info "Screenshots coming"
    These steps are described in words for now; annotated screenshots land once the screens
    are final.

## Invite a volunteer or advocate

1. Open **Volunteers** and choose **Invite**.  <!-- @frontend: confirm the nav label and invite control -->
2. Enter the person's **email** and the **role** they'll have.
3. Send the invite. They receive an email to
   [accept and set a password](../account/accept-invite.md). Invites expire (typically
   after 7 days).

## Assign a volunteer to a family

A volunteer can see **only the family they're assigned to** — so the assignment is what
gives them access.

1. Open the volunteer's profile.
2. **Assign** them to a family.  <!-- @frontend: confirm the assign control and whether it's one family at a time -->
3. Save. They can now see that family's needs, schedule, and messages — and nothing else.

## Set roles & statuses

1. Open the person's profile.
2. Set their **status** (where they are in their journey — for example *Prospect*,
   *Serving*) and any details like support type or childcare approval.
   → [Statuses explained](../../reference/statuses.md)
3. To give a volunteer extra abilities within their family, mark them a **Lead Volunteer**.
   A lead can do more (such as create or remove needs) but is still limited to that one
   family.

## Activate a trained volunteer

When someone finishes their training they become **trained but not yet active**. To let
them start serving:

1. Open the **awaiting activation** list (trainees who finished training).
   <!-- @frontend: confirm where this list lives (Volunteers page section?) and its label -->
2. Open the person and **activate** them.
3. Assign them to a family if you haven't already.

## Related

- [Onboard a family & invite people](onboarding.md)
- [Manage families & people](families-and-people.md)
- [Roles & permissions matrix](../../reference/permissions-matrix.md)
