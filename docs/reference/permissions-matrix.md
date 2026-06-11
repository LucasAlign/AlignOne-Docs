---
status: needs-review
primary: backend
---

# Roles & permissions matrix

What each role can see and do. Visibility is enforced by the server on every request — see
[Roles & who sees what](../concepts/roles-and-visibility.md) for how scope is decided.

<!-- @frontend: confirm role names and that the UI matches these capabilities. -->
<!-- @backend: re-confirm the Family-role action cells (marked c) against the handlers in a later pass. -->

| Capability | Admin | Coordinator | Advocate | Volunteer | Family |
|---|:---:|:---:|:---:|:---:|:---:|
| See **all** families | ✓ | ✓ | — | — | — |
| See families at **their church** | ✓ | ✓ | ✓ | — | — |
| See **one** family (assigned / own) | ✓ | ✓ | ✓ ᵃ | ✓ | ✓ |
| Browse & claim needs | ✓ | ✓ | ✓ | ✓ | — |
| Create / remove needs | ✓ | ✓ | ✓ | Lead ᵇ | ✓ ᶜ |
| Schedules: view & sign up | ✓ | ✓ | ✓ | ✓ | ✓ ᶜ |
| Messaging within a circle | ✓ | ✓ | ✓ | ✓ | ✓ ᶜ |
| Manage families, volunteers, churches | ✓ | ✓ | their church ᵃ | — | — |
| Invite / onboard people | ✓ | ✓ | ✓ | — | — |
| View the audit log | ✓ | ✓ | — | — | — |

**✓** = allowed · **—** = not available

- **ᵃ** Across each family their church serves.
- **ᵇ** A **Lead Volunteer** can create/remove needs within their one family.
- **ᶜ** Within their own family's circle. Exact Family-role actions are being confirmed.
