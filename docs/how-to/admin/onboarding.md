---
status: needs-ui
primary: frontend
---

<!-- @backend verified: onboarding is email-invite based; invite links are secure and
     expire (typically 7 days). A newly self-registered family starts at "Care Requested /
     Needs Vetting" and must be approved by staff before becoming active. -->

# Onboard a family & invite people

**Who this is for:** Program staff (Admins and Coordinators); advocates for their church.
**When to use it:** When you bring a new family into AlignOne and invite the people who'll
support them.
**Before you start:** You're signed in with staff access.

!!! info "Screenshots coming"
    These steps are described in words for now; annotated screenshots land once the screens
    are final.

## Onboard a family

1. [Create the family record](families-and-people.md) — parents, children, and the
   primary contact.
2. Connect it to the right **county** and **serving church** so the correct advocate can
   see it. → [Manage churches & counties](organizations.md)
3. [Invite and assign volunteers](volunteers-and-advocates.md) to begin support.

### Approving a self-registered family

A family that **registers itself** doesn't go live automatically. It starts at
**Care Requested / Needs Vetting** and waits for staff to review it.

1. Open the family from the pending/vetting list.
   <!-- @frontend: confirm where families awaiting vetting appear and the label -->
2. Review the details, then **approve** the family to move it into active service.
   → [Statuses explained](../../reference/statuses.md)

## Send account setup emails to a family's parents

**Who can do this:** Admins, Coordinators, and Advocates (for families their church serves).

When a family was **imported or created by staff**, its parents exist in AlignOne but have
never signed in — they have no login yet. Use **Send Account Setup Emails** to create
their accounts and email them everything they need to sign in.

1. Open the family from **Families** and switch to the **Household** tab.
2. Select **Send Account Setup Emails**.
3. Review the confirmation: parents **with an email on file** are listed as recipients;
   parents **without an email** are skipped. If someone is missing, close the dialog,
   [add their email to the parent record](families-and-people.md), and try again.
4. Confirm to send. Each parent receives an email with a **temporary password** and a
   sign-in link. On their first sign-in, AlignOne asks them to set a permanent password.
5. Check the per-parent results:
    - **Email sent** — all set; the parent can sign in.
    - **Already has an account** — nothing was sent; they can sign in as usual.
    - **No email on file** — add an email to the parent record first.
    - **Email failed** — the account **was** created, but the email couldn't be
      delivered. Use **Copy Message** to copy a ready-to-send sign-in message (including
      the temporary password) and email it to the parent yourself.

!!! tip "Safe to press again"
    Sending is skipped for any parent who already has an account, so re-running this for
    a family never duplicates logins or resets existing passwords.

## Invite a person

1. From **Volunteers**, choose **Invite** and enter the person's email and role.
   → [Manage volunteers & advocates](volunteers-and-advocates.md)
2. They get an email to [accept and set a password](../account/accept-invite.md).

## Resend an invite

If someone didn't get their invite or it expired:

1. Open the person's record.
2. Choose **Resend invite**.  <!-- @frontend: confirm the resend control and label; confirm whether it reissues a fresh expiry -->
3. A new invite email goes out.

!!! tip "Invites expire"
    Invite links are time-limited (typically 7 days). If someone waited too long, resend
    rather than troubleshooting the old link.

## Related

- [Manage families & people](families-and-people.md)
- [Manage volunteers & advocates](volunteers-and-advocates.md)
- [Troubleshooting](../../reference/troubleshooting.md)
