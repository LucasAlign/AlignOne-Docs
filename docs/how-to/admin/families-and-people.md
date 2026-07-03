---
status: needs-ui
primary: frontend
---

<!-- @backend verified: a "community" IS a family (1:1 merge); the family is the WrapAround
     care circle. Family records hold parents and children; one parent is the primary contact.
     CSV import of families is supported and every import is written to the audit log. -->

# Manage families & people

**Who this is for:** Program staff (Admins and Coordinators); advocates for their church's
families.
**When to use it:** When you set up a new family or update who's in one.
**Before you start:** You're signed in with staff access.

!!! info "Screenshots coming"
    These steps are described in words for now; annotated screenshots land once the screens
    are final.

## The family is the care circle

In AlignOne a **family** *is* the WrapAround care circle — everything else is organized
around it. A family record holds its **parents** and **children**, with one parent set as
the **primary contact**.

## Add a family

1. Open **Families** and choose **Add family**.  <!-- @frontend: confirm the nav label and the add button -->
2. Enter the family's details, then add **parents** and **children**.
   <!-- @frontend: confirm the fields for family, parent, and child -->
3. Set one parent as the **primary contact** — the main point of contact for the circle.
4. **Save.** The family is created and ready for volunteers and a schedule.

Parents added this way don't have a login yet — when the family is ready, [send them
account setup emails](onboarding.md#send-account-setup-emails-to-a-familys-parents).

## Update a family

1. Open the family from **Families**.
2. Edit the family's details, add or remove **parents/children**, change the
   **primary contact**, or [upload a family photo](#upload-a-family-photo).
3. **Save** your changes.

## Upload a family photo

1. Open the family and select its **photo**.
2. Choose an image and confirm to upload.
   <!-- @frontend: confirm the control and any file-type/size limits -->

## Import many families at once

For setup or migration you can **import families from a CSV** instead of adding them one by
one.

1. Open the **import** tool and download the **family template**.
   <!-- @frontend: confirm where import lives and the template download -->
2. Fill in the template — including parents and children — and upload it.
3. Review the result. Every import is recorded in the **audit log**.
4. Imported parents can't sign in yet — open each family and
   [send account setup emails](onboarding.md#send-account-setup-emails-to-a-familys-parents)
   when you're ready to bring them into the portal.

!!! warning "Never use real PII in examples or templates you share"
    Family information is sensitive. Keep filled-in import files secure and out of shared
    locations.

## Related

- [Manage volunteers & advocates](volunteers-and-advocates.md)
- [Onboard a family & invite people](onboarding.md)
- [Manage churches & counties](organizations.md)
- [Oversight](oversight.md)
