# MINAYO OPS: Decision Register

Last updated: 2026-10-31

Rule: unresolved items are never silently turned into requirements. Each item below has an owner, an impact and a required resolution.

Owner key: **PO** = product owner (Super Admin). **Legal** = Nigerian legal and regulatory advice. **Provider** = the external service named.

---

## A. Resolved decisions

| ID | Decision | Detail | Date |
|---|---|---|---|
| R1 | Commission split | Freelance contracts: 10% total, charged as 5% to the client (added on top of the agreed price) and 5% to the freelancer (deducted from their payout). Marketplace: 5%, deducted from the seller. Percentages apply to the agreed contract or order amount. Rates stay configurable by authorised Admins and apply to new transactions only. **Worked example awaiting PO confirmation:** ₦100,000 contract, client pays ₦105,000, freelancer receives ₦95,000, platform keeps ₦10,000. | 2026-10-31 |
| R2 | Full-time job listings | Listing and application tracking only at launch. No contract, funding or commission flow. Contracts and payments apply to freelance work. | 2026-10-31 |
| R3 | Who can sell | Both Clients and Freelancers can sell on the marketplace. Every new listing needs Admin approval. No further seller requirements are defined; identity verification stays optional. | 2026-10-31 |
| R4 | Accounts | One ordinary account type per email address (Client or Freelancer), never changeable. A person who wants both uses a second email. | 2026-10-31 |

Consequences of R1 to R3 for the design:
- Freelance contracts need two commission records, one per party, each with its own rate snapshot.
- Marketplace selling is a capability available to both account types, not tied to Freelancer.
- This supersedes handover sections 11 and 25 where they say only freelancers sell.

---

## B. Open decisions

| ID | Decision needed | Owner | Impact | Required resolution | Blocks |
|---|---|---|---|---|---|
| O1 | Legal and technical fund-custody arrangement, including Paystack's exact ability to support payment, refund and payout workflows. Also covers client wallet balances and client withdrawals | Legal, Provider | Critical | Written legal confirmation and provider confirmation | Live funding and payouts (Phase 6) |
| O2 | Identity verification provider | PO | Medium | Select a provider | Enabling verification |
| O3 | Marketplace payment-release rule after revised delivery | PO | High | Decide review-period treatment | Marketplace payments live |
| O4 | Responsibility for gateway charges on refunds | PO, Legal | High | Decide who bears them | Refund flows (Phase 6) |
| O5 | Automatic logout duration after inactivity | PO | Low | Choose a duration | Phase 1 |
| O6 | Support hours and response-time targets | PO | Low | Define hours and targets | Phase 8 |
| O7 | Data retention periods | Legal | High | Legal advice | Phase 1 deletion rules |
| O8 | Minor safeguards and consent | Legal | High | Legal advice | Phase 1 registration |
| O9 | Dispute appeal deadlines | PO | Medium | Choose a deadline | Phase 5 |
| O10 | Payment reconciliation intervals and escalation process | PO | High | Define intervals and escalation | Phase 6 |
| O11 | Hosting, storage, email, SMS and monitoring budgets | PO | Medium | Approve a budget | Phase 8 and launch |
| O12 | Email and SMS provider configuration (Resend, Termii) | PO | Low | Account setup and sender details | Phase 8 |
| O13 | Whether the client-side 5% commission is refunded when a contract is cancelled before work begins (the PRD says the client gets a full refund) | PO | High | Decide, together with O4 | Phase 6 |

---

## C. Scope notes (PRD vs handover alignment)

Added to the plan although the handover did not list them:
- Platform-owned job postings by admins
- Automated flagging of suspicious job posts for review
- Guided onboarding with a skip option
- The four published policies (Prohibited Activities, Fair Usage, Dispute Resolution, Code of Conduct)
- Downloadable contracts and receipts
- Financial reports exportable to Excel and PDF
- Mutual deadline extensions, not only freelancer-initiated
- Client wallets with withdrawal of unused funds (also gated by O1)

Deferred past the first build:
- Personalised marketplace recommendations

Naming: the client navigation item is "Contracts" (PRD wording).
