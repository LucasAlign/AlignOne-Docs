---
status: needs-review
primary: backend
---

# Roles & permissions matrix

What each role can see and do. Visibility is enforced by the server on every request — see
[Roles & who sees what](../concepts/roles-and-visibility.md) for how scope is decided.

<!-- @frontend: confirm role names and that the UI matches these capabilities. -->

| Capability | Admin | Coordinator | Advocate | Volunteer | Family |
|---|:---:|:---:|:---:|:---:|:---:|
| See **all** families | ✓ | ✓ | — | — | — |
| See families at **their church** | ✓ | ✓ | ✓ | — | — |
| See **one** family (assigned / own) | ✓ | ✓ | ✓ ᵃ | ✓ | ✓ |
| View needs & schedules (in scope) | ✓ | ✓ | ✓ | ✓ | ✓ |
| Claim a need | ✓ | ✓ | ✓ | ✓ | — ᵈ |
| Create / edit / delete needs | ✓ | ✓ | ✓ | Lead only ᵇ | — |
| Create / edit / delete schedules | ✓ | ✓ | — | — | — |
| Invite / onboard people | ✓ | ✓ | ✓ | — | — |
| Manage families, volunteers, churches | ✓ | ✓ | their church ᵃ | — | — |
| View the audit log | ✓ | ✓ | — | — | — |

**✓** = allowed · **—** = not available

- **ᵃ** Across each family their church serves.
- **ᵇ** A **Lead Volunteer** can create/edit/delete needs within their one family; other volunteers cannot.
- **ᵈ** Claiming is for helpers — a family sees the needs raised for them but doesn't claim them.

Families have a **read-only** view of their own circle: they can see their family, its
needs, and its schedule, but care tasks are created and claimed by volunteers, advocates,
and staff. Only admins and coordinators create or change the schedule.
