 MINAYO OPS
 COMPLETE TECHNICAL DEVELOPMENT HANDOVER & CLAUDE MASTER PROMPT

Project: MINAYO OPS  
Product: Freelance, Recruitment and Digital Marketplace Platform  
Initial Market: Nigeria  
Currency: Nigerian Naira (₦)  
Primary Language: English  
Development Assistant: Claude  
Development Approach: Structured, phased implementation

---

 PART ONE — PROJECT FOUNDATION

 1. PROJECT OVERVIEW

MINAYO OPS is an integrated digital platform connecting clients with skilled freelancers while providing recruitment, contract management, payment management and a digital marketplace.

The two ordinary account types are:

- Client
- Freelancer

Administrative roles:

- Super Admin
- Admin
- Moderator
- Support Staff
- Finance Staff

The platform must support:

- Job opportunities and recruitment.
- Professional freelancer profiles.
- Messaging and negotiations.
- Offers and contracts.
- Milestones and revisions.
- Wallets and financial records.
- Payments, refunds and withdrawals.
- Dispute resolution.
- Digital products and services marketplace.
- Ratings and reviews.
- Administrative management.
- Customer support.
- Platform analytics.

This is not a simple job board or a frontend demonstration. It is intended to become a complete, scalable digital platform.

 2. APPROVED TECHNOLOGY STACK

Use the following technologies unless a genuine technical limitation requires a documented alternative.

| Technology | Purpose |
|---|---|
| Next.js | Main application framework |
| TypeScript | Application programming language |
| Tailwind CSS | Styling and responsive layouts |
| Supabase | PostgreSQL database, authentication and file storage |
| Vercel | Hosting and deployment |
| GitHub | Source code management |
| Paystack | Payment gateway |
| Resend | Transactional email |
| Termii | SMS and OTP delivery |
| Sentry | Error monitoring |
| PostHog | Product analytics |

Use stable, mutually compatible versions.

Prefer free or low-cost tiers during initial development. Do not introduce unnecessary paid dependencies.

 3. APPLICATION ARCHITECTURE

Use a modular monolithic architecture.

The application should have one main Next.js codebase, with features separated into independent modules.

Use:

- Next.js App Router.
- TypeScript.
- Server Components where appropriate.
- Client Components where interactivity requires them.
- Server Actions or protected API routes.
- Supabase PostgreSQL.
- Supabase Auth.
- Supabase Storage.
- Supabase Row Level Security.
- Vercel deployment.

Avoid introducing microservices at launch unless a documented technical requirement justifies them.

---

 PART TWO — DATABASE DESIGN

 4. DATABASE PRINCIPLES

Design the database before implementing the complete application.

The database must:

- Maintain referential integrity.
- Use appropriate foreign keys and constraints.
- Include creation and update timestamps.
- Support soft deletion where appropriate.
- Protect sensitive information.
- Support financial reconciliation.
- Avoid unnecessary duplication.
- Support future expansion.

Use UUID primary keys where appropriate.

Use exact decimal or integer minor-unit representations for financial amounts. Never use floating-point arithmetic for money.

Store timestamps consistently in UTC and display them using each user's selected time zone.

 5. PROPOSED DATABASE ENTITIES

The following is an initial logical inventory, not an instruction to create every table immediately.

Identity and accounts
- profiles
- user_roles
- user_preferences
- user_sessions
- verification_submissions
- account_deletion_requests
- user_blocks
- user_reports
- user_consents
- policy_versions

Freelancer profiles
- freelancer_profiles
- freelancer_skills
- skills
- portfolio_items
- work_experiences
- education_records
- freelancer_services
- profile_visibility_settings

Jobs and recruitment
- job_categories
- jobs
- job_skills
- job_applications
- application_attachments
- application_shortlists
- application_invitations
- application_status_history

Messaging and offers
- conversations
- conversation_participants
- messages
- message_attachments
- message_reports
- offers
- offer_history

Contracts and delivery
- contracts
- contract_participants
- contract_acceptances
- contract_terms
- contract_milestones
- milestone_submissions
- revision_requests
- deadline_extension_requests
- contract_cancellations
- contract_deliverables
- contract_status_history

Financial operations
- wallet_accounts
- wallet_transactions
- financial_ledger_entries
- payment_transactions
- payment_events
- payment_reconciliations
- refunds
- withdrawal_requests
- bank_accounts
- commission_settings
- commission_records
- payment_receipts
- financial_invoices

Marketplace
- marketplace_categories
- marketplace_listings
- marketplace_listing_media
- marketplace_licenses
- marketplace_orders
- marketplace_order_items
- marketplace_deliveries
- marketplace_revision_requests
- marketplace_order_disputes
- marketplace_downloads
- marketplace_reviews

Reviews and disputes
- reviews
- review_responses
- review_reports
- disputes
- dispute_evidence
- dispute_decisions
- dispute_appeals
- dispute_status_history

Notifications and support
- notifications
- notification_preferences
- announcements
- announcement_reads
- support_tickets
- support_ticket_messages
- support_assignments
- email_logs
- sms_logs

Administration and content
- admin_actions
- audit_logs
- platform_settings
- platform_policies
- faq_categories
- faqs
- help_articles
- blog_posts
- social_links
- referral_codes
- referral_tracking
- maintenance_settings

Analytics and operations
- analytics_events
- system_events
- scheduled_tasks
- integration_logs

Claude must review this inventory, consolidate overlapping entities and produce the final relational schema.

Do not create unnecessary tables simply to match this list.

 6. IMPORTANT RELATIONSHIPS

Preserve the following relationships:

- One user has one primary profile.
- A user has one ordinary account type: Client or Freelancer.
- Administrative permissions are managed separately.
- Freelancers can have multiple skills, portfolio items and experiences.
- Clients can create multiple jobs.
- Jobs can receive multiple applications.
- Applications belong to one freelancer and one job.
- Conversations have defined participants.
- Offers belong to the relevant client, freelancer and negotiation.
- Contracts have two primary parties.
- Contracts can have multiple milestones.
- Contracts can have multiple revision and extension requests.
- Contracts can have multiple financial records.
- Marketplace listings belong to sellers.
- Marketplace orders belong to buyers and contain relevant order items.
- Disputes reference the relevant contract or marketplace order.
- Reviews reference verified eligible transactions.
- Financial ledger entries are traceable to their source transactions.

Use database constraints to prevent invalid states.

---

 PART THREE — SECURITY AND ACCESS CONTROL

 7. AUTHENTICATION

Implement:

- Email and password registration.
- Email verification.
- Login and logout.
- Password reset.
- Google sign-in.
- Secure session management.
- Optional two-factor authentication for ordinary users.
- Mandatory two-factor authentication for Super Admin accounts.

Registration must allow users to select Client or Freelancer.

Users must not be able to change their account type by manipulating browser requests or database values.

 8. ROLE-BASED ACCESS CONTROL

Super Admin: Full administrative control. Only the Super Admin can access the audit log.

Admin: Access to assigned operational management functions.

Moderator: Access to assigned reports, listings and moderation functions.

Support Staff: Access to assigned support tickets and permitted user-support information.

Finance Staff: Access to assigned financial operations and records.

Enforce permissions on the server and at the database level.

Hiding buttons in the frontend is not sufficient access control.

 9. SUPABASE ROW LEVEL SECURITY

Enable and configure Row Level Security on all user-accessible tables.

Examples:

- Freelancers can edit their own profiles.
- Clients can manage their own job postings.
- Freelancers can access their own applications.
- Conversation participants can access permitted messages.
- Contract parties can access their contracts.
- Only authorised parties can submit revisions or approve work.
- Users can access only their permitted wallet information.
- Sellers can manage their own listings.
- Buyers can access their own orders.
- Dispute evidence is restricted to authorised parties and Admin investigators.
- Administrative operations require appropriate permissions.

Service-role credentials must never be exposed to the browser.

Sensitive documents must use private storage buckets and appropriately restricted access.

---

 PART FOUR — PRODUCT FUNCTIONALITY

 10. PUBLIC WEBSITE

Build:

- Landing page.
- About Us.
- Contact Us.
- Blog and News.
- Public freelancer profiles.
- Public marketplace listings.
- Public opportunity previews.

Visitors can view permitted public content without registering.

Anyone wishing to apply for an opportunity or use account-restricted functionality must register and log in.

 11. FREELANCER DASHBOARD

Main navigation:

1. Find Work.
2. My Contracts.
3. Messages.
4. Marketplace.

Hamburger menu:

- My Profile.
- Wallet.
- About.
- Support.

Freelancers can:

- Search and filter opportunities.
- Save opportunities.
- Apply for jobs.
- Withdraw applications before hiring.
- Receive and respond to invitations.
- Negotiate offers.
- Manage contracts.
- Submit work.
- Request deadline extensions.
- Respond to revision requests.
- View earnings.
- Withdraw available balances.
- Sell marketplace products and services.

Display profile completion percentage.

Incomplete profiles may apply, but should receive a notice explaining that completing their profile may improve hiring chances.

 12. CLIENT DASHBOARD

Main navigation:

1. Post Work.
2. Hire Talent.
3. Contract.
4. Messages.
5. Marketplace.

Hamburger menu:

- My Profile.
- Wallet.
- About.
- Support.

Clients can:

- Post opportunities.
- Manage job postings.
- Review and shortlist applicants.
- Invite freelancers.
- Compare applicants.
- Negotiate prices.
- Accept final offers.
- Manage contracts.
- Fund contracts.
- Approve work.
- Request revisions.
- Report problems.
- Purchase marketplace products and services.

Clients must not access the freelancer jobs feed as job-seeking users.

 13. JOB AND APPLICATION WORKFLOW

Application statuses:

- Submitted.
- Under Review.
- Shortlisted.
- Interview.
- Offer Received.
- Hired.
- Rejected.
- Withdrawn.

Clients can shortlist and reject applicants.

Freelancers can withdraw applications before hiring.

Clients can invite freelancers to apply.

Interview invitations generate immediate notifications.

Accepting an interview invitation opens a text-based conversation.

Voice and video interviews are not required at launch.

Clients can compare applicants, including relevant rate information.

Once applications have started, important job terms cannot be edited. Clients must close the existing posting and create a new one to change important terms.

Jobs automatically close at their application deadlines.

---

 PART FIVE — CONTRACTS AND PAYMENTS

 14. CONTRACT WORKFLOW

Implement this sequence:

1. Client and freelancer negotiate.
2. Client makes a final offer.
3. Freelancer accepts.
4. System generates the contract.
5. Both parties digitally accept.
6. Contract becomes active.
7. Client funds the contract.
8. System confirms required funds are secured.
9. Freelancer begins work.

Contracts must contain project scope, deliverables, agreed amount, deadline, revision allowance, payment structure, milestones and agreed terms.

 15. REVISIONS

Free revision limits must be agreed and stated in the contract before work begins.

Additional revisions require negotiation of an additional fee.

Maintain records of revision requests and responses.

 16. DEADLINES

Freelancers can request extensions before deadlines expire.

Extensions require client approval.

The updated deadline must be recorded.

Unapproved late delivery can be reported to Admin.

 17. MILESTONES

Clients fund the entire contract upfront.

Where milestones exist, allocate the funded contract amount across the agreed milestones.

Approved milestone submissions trigger the applicable payout process.

Payment remains pending while revisions or reported problems are unresolved.

 18. CONTRACT COMPLETION

After final submission, the client has seven days to:

- Approve.
- Request revisions.
- Report a problem.

If the client takes no action within seven days, the contract automatically moves to Completed and the applicable payout is triggered.

Automatic completion must be reliable, auditable and protected against duplicate payouts.

 19. CANCELLATION

Before work begins, approved cancellation results in a full client refund.

After work begins, Admin determines the fair refund based on completed work, contract terms, evidence and circumstances.

Freelancer abandonment can be reported and investigated.

 20. DISPUTES

Both parties can submit evidence, including messages, files, screenshots and contract terms.

Funds remain on hold during investigation.

Admin should aim to resolve disputes within 5–7 working days.

Both parties receive progress updates.

Either party may appeal a decision.

---

 PART SIX — FINANCIAL SYSTEM

 21. WALLET ARCHITECTURE

Build a transaction-ledger-based financial system.

Do not rely on editable balance numbers.

All balance changes must be represented by traceable financial entries.

Separate:

- Available balances.
- Pending balances.
- Reserved or allocated balances.
- Deposits.
- Earnings.
- Withdrawals.
- Refunds.
- Commissions.

Use atomic database operations and idempotency controls to prevent duplicate financial actions.

 22. COMMISSIONS

Freelance contract commission: 10%.

Marketplace commission: 5%.

Commission rates must be configurable by authorised Admins.

Changes apply to new transactions only.

Existing contracts and orders retain their agreed rates.

Display applicable charges before payment confirmation.

Maintain separate reporting for freelance and marketplace commissions.

 23. PAYSTACK

Integrate Paystack using supported APIs and verified payment events.

Implement:

- Payment initialisation.
- Payment verification.
- Webhook handling.
- Reconciliation.
- Refund initiation.
- Refund tracking.
- Transaction logging.
- Failure handling.

Never trust a frontend success message as proof of payment.

Verify payment status server-side.

Delayed notifications must trigger reconciliation before a transaction is considered failed.

Confirmed unsuccessful transactions must enter the appropriate refund process.

Users must receive payment status updates.

Critical dependency: The proposed fund-separation, holding and payout arrangement must be legally and technically validated for Nigeria.

Do not assume a standard Paystack merchant account automatically provides compliant escrow or custodial services.

Do not enable live contract funding or payout functionality until the arrangement is approved.

Build a payment-provider abstraction so an approved alternative can be integrated if necessary.

 24. WITHDRAWALS

Freelancers can withdraw all eligible available balances.

There is no minimum withdrawal threshold at launch.

Validate bank details and account ownership.

Withdrawals should be automatic after required checks.

Suspicious withdrawals can be held or rejected by authorised Admins.

---

 PART SEVEN — MARKETPLACE

 25. MARKETPLACE FUNCTIONALITY

Allow users to sell:

- Digital products.
- Design assets.
- Templates.
- Digital documents.
- Creative services.
- Other permitted digital offerings.

New listings require Admin approval.

Significant edits require re-review.

Sellers set delivery timelines.

Sellers specify personal, commercial or extended usage rights.

Apply buyer-specific identifying details or watermarks where technically possible.

Eligible purchased products should be available for re-download.

 26. MARKETPLACE ORDERS

Marketplace commission: 5%.

Buyers receive seven days after delivery to inspect an order.

They can accept, request revisions or report problems.

Revision requests pause the review period until resubmission.

Reported problems keep funds on hold pending Admin resolution.

If the buyer takes no action within seven days, refer the order to Admin before releasing funds.

The precise review-period treatment after revised delivery must remain configurable until the final policy is approved.

---

 PART EIGHT — OTHER PLATFORM FEATURES

 27. RATINGS AND REVIEWS

Clients and freelancers can review one another after verified completed contracts.

Use 1–5 star ratings and optional written comments.

Support public responses and review reporting.

Marketplace reviews must be tied to eligible purchases.

Prevent fake and duplicate reviews.

 28. NOTIFICATIONS

Support:

- In-app notifications.
- Email.
- Push notifications.
- SMS for selected critical events.

Users can control ordinary notification preferences.

Critical security notifications remain enabled.

Announcements stay in history and support read/unread status.

 29. SUPPORT

Implement support tickets, assignments, responses, status changes and notifications.

Display support hours and expected response times.

 30. ADMINISTRATION

Build administrative modules for:

- User management.
- Verification.
- Job monitoring.
- Applications.
- Contracts.
- Disputes.
- Marketplace approval.
- Financial operations.
- Withdrawals.
- Refunds.
- Commission configuration.
- Support tickets.
- Blog and content management.
- FAQs and Help Centre.
- Announcements.
- Analytics.
- Platform settings.

Only the Super Admin can access the audit log.

 31. OTHER REQUIREMENTS

Implement:

- Dark and Light Mode.
- Dashboard customisation.
- Bookmarks.
- Adjustable text size.
- Accessibility.
- PWA installation.
- SEO for public pages.
- Referral tracking without cash rewards at launch.
- Analytics.
- Daily database backups.
- Maintenance mode.
- Error and uptime monitoring.
- Account deactivation and deletion.
- Data export.
- Login activity.
- Cookie consent controls.
- Policy acceptance and version tracking.

The platform launches in English and Naira only.

Use automatic time-zone detection with manual preference.

Use a standard number format and user-selectable date format.

---

 PART NINE — DESIGN SYSTEM

 32. VISUAL DIRECTION

Use the following brand palette:

- Black.
- White.
- Cream.
- Dark Blue.
- Subtle Gold.

Use Montserrat as the primary brand font.

The interface should feel modern, premium, professional and approachable.

Use gold sparingly for highlights rather than as the dominant interface colour.

 33. DESIGN PRINCIPLES

- Mobile-first.
- Responsive.
- Clear navigation.
- Consistent spacing.
- Accessible contrast.
- Reusable components.
- Clear buttons and forms.
- Helpful loading and error states.
- Consistent dashboard layouts.
- Fast interactions.

The Super Admin should have an appearance editor for approved platform colours, fonts and light/dark appearance settings.

Saved changes must propagate across the platform.

Use validated design tokens rather than arbitrary unsafe CSS injection.

---

 PART TEN — PROJECT STRUCTURE

 34. PROPOSED FOLDER STRUCTURE

```text
minayo-ops/
│
├── app/
│   ├── (public)/
│   ├── (auth)/
│   ├── (client)/
│   ├── (freelancer)/
│   ├── (admin)/
│   ├── api/
│   └── layout.tsx
│
├── components/
│   ├── ui/
│   ├── forms/
│   ├── navigation/
│   ├── dashboards/
│   └── shared/
│
├── features/
│   ├── authentication/
│   ├── profiles/
│   ├── jobs/
│   ├── applications/
│   ├── messaging/
│   ├── offers/
│   ├── contracts/
│   ├── payments/
│   ├── wallets/
│   ├── marketplace/
│   ├── disputes/
│   ├── reviews/
│   ├── notifications/
│   └── administration/
│
├── lib/
│   ├── supabase/
│   ├── paystack/
│   ├── email/
│   ├── sms/
│   ├── security/
│   ├── validation/
│   └── utilities/
│
├── services/
├── hooks/
├── types/
├── config/
├── supabase/
│   ├── migrations/
│   ├── seed.sql
│   └── tests/
│
├── public/
├── tests/
└── documentation/
```

This is a proposed structure. Claude may improve it while preserving clear separation of concerns.

---

 PART ELEVEN — IMPLEMENTATION ROADMAP

 35. DEVELOPMENT PHASES

The platform must be built in controlled phases.

Do not attempt to generate the entire platform in one uncontrolled operation.

 PHASE 0 — Project Setup

- Create the Next.js project.
- Configure TypeScript.
- Configure Tailwind CSS.
- Connect GitHub.
- Configure Vercel.
- Connect Supabase.
- Configure environment variables.
- Establish development, staging and production environments.
- Create initial documentation.

Completion condition: The project builds and deploys successfully without exposed secrets.

 PHASE 1 — Database and Authentication

- Finalise the relational schema.
- Create database migrations.
- Configure Supabase Auth.
- Build registration and login.
- Add Google sign-in.
- Implement Client and Freelancer roles.
- Implement administrative permissions.
- Configure RLS.
- Test access restrictions.

Completion condition: Authentication and permission tests pass.

 PHASE 2 — UI Foundation

- Build design tokens.
- Build reusable components.
- Build responsive navigation.
- Build landing page.
- Build public pages.
- Build Client dashboard shell.
- Build Freelancer dashboard shell.
- Build Admin dashboard shell.
- Implement Light and Dark Mode.

Completion condition: Major interface foundations are responsive and consistent.

 PHASE 3 — Profiles and Recruitment

- Freelancer profiles.
- Client profiles.
- Skills and portfolios.
- Job creation.
- Job discovery.
- Applications.
- Shortlisting.
- Invitations.
- Application management.

Completion condition: Recruitment workflow works end to end.

 PHASE 4 — Messaging and Offers

- Conversations.
- Messages.
- Attachments.
- Notifications.
- Interview invitations.
- Negotiations.
- Offers.
- Offer acceptance.

Completion condition: Clients and freelancers can complete negotiations and generate final offers.

 PHASE 5 — Contracts

- Contract generation.
- Digital acceptance.
- Contract activation.
- Milestones.
- Revisions.
- Deadline extensions.
- Deliverables.
- Contract completion.
- Cancellation.
- Disputes.

Completion condition: Contract workflows pass end-to-end tests using simulated payments.

 PHASE 6 — Financial System

- Wallet records.
- Financial ledger.
- Payment integration.
- Payment verification.
- Webhooks.
- Reconciliation.
- Refund tracking.
- Withdrawals.
- Commission calculations.
- Financial reports.

Completion condition: Test transactions, duplicate events, failed payments, refunds and payout simulations are handled correctly.

Live payment release remains blocked until the fund-handling arrangement is validated.

 PHASE 7 — Marketplace

- Listings.
- Admin approval.
- Search and filtering.
- Orders.
- Delivery.
- Revisions.
- Licensing.
- Downloads.
- Reviews.
- Disputes.

Completion condition: Marketplace buying and selling works in a test environment.

 PHASE 8 — Admin, Support and Notifications

- Admin tools.
- Moderation.
- Support tickets.
- Announcements.
- Content management.
- FAQs.
- Blog.
- Notification preferences.
- Email and SMS integrations.

Completion condition: Administrative workflows and notifications work correctly.

 PHASE 9 — Security and Quality Assurance

- Security testing.
- RLS testing.
- Payment testing.
- Accessibility testing.
- Performance testing.
- Backup and restore testing.
- Error monitoring.
- Mobile responsiveness.
- Concurrent-user testing.

Completion condition: No unresolved critical security or financial defects.

 PHASE 10 — Beta and Launch

- Deploy to staging.
- Invite selected testers.
- Collect feedback.
- Fix issues.
- Validate integrations.
- Obtain Super Admin production approval.
- Deploy to production.
- Open public registration.

Completion condition: Production platform is approved and ready for users.

---

 PART TWELVE — OUTSTANDING DECISIONS

 36. DO NOT GUESS THESE ITEMS

The following require technical, commercial or regulatory validation:

1. Legal and technical fund-custody arrangement.
2. Paystack's precise ability to support payment, refund and payout workflows.
3. Identity verification provider.
4. Marketplace review-period behaviour after revised delivery.
5. Treatment of payment gateway charges during refunds.
6. Exact inactivity logout duration.
7. Support operating hours and response-time targets.
8. Legally required data retention periods.
9. Safeguards and consent requirements for minors.
10. Email and SMS provider configurations.
11. Dispute appeal deadlines.
12. Final production hosting and storage costs.

Maintain a decision register documenting each unresolved item, its owner, impact and required resolution.

Do not silently convert unresolved decisions into confirmed requirements.

---

 PART THIRTEEN — CLAUDE MASTER PROMPT

 37. MASTER DEVELOPMENT INSTRUCTION

You are the lead software architect, senior full-stack engineer, database designer, security engineer and technical project manager responsible for developing MINAYO OPS.

You are not being asked to create a simple landing page, prototype or visual demonstration.

You are responsible for helping build a complete, production-oriented freelance, recruitment and digital marketplace platform according to the approved MINAYO OPS PRD and this technical handover.

 A. PRIMARY RESPONSIBILITY

Study the complete PRD and technical handover.

Treat both as the primary sources of truth.

The PRD defines what MINAYO OPS must do.

This technical handover defines the proposed architecture, database design, implementation principles and development roadmap.

Where the documents overlap, preserve their requirements.

Where a genuine conflict exists, identify it and request clarification instead of silently choosing an interpretation.

 B. CRITICAL DEVELOPMENT APPROACH — DO NOT BUILD EVERYTHING AT ONCE

This is a major instruction.

Do not attempt to build the entire MINAYO OPS platform in one response, one code-generation operation or one uncontrolled development session.

Do not immediately generate every database table, every dashboard, every API route and every feature simply because they appear in the specification.

The proposed database inventory is a starting point, not an instruction to create more than 100 tables immediately.

Instead, follow this controlled process:

1. Inspect the available project environment and existing repository.
2. Understand the complete product requirements.
3. Review the proposed architecture.
4. Identify dependencies and technical risks.
5. Finalise the database schema based on actual relationships and workflows.
6. Separate essential launch functionality from later enhancements.
7. Establish the project foundation.
8. Implement one development phase at a time.
9. Test each phase before proceeding.
10. Update the documentation and progress record.

Avoid creating tables, components, services or abstractions that have no clear purpose in the current implementation.

Do not build placeholder features merely to make the platform appear complete.

Do not rush into later phases while the current phase has unresolved critical defects.

The priority is correctness, security, maintainability and a genuinely working product—not the number of files or features generated.

 C. PHASE APPROVAL AND CHECKPOINTS

Use the development roadmap in this handover.

At the beginning of each phase:

- Explain its objectives.
- Identify dependencies.
- State what will be implemented.
- Identify risks and external requirements.

At the end of each phase:

- Report completed functionality.
- List files created or modified.
- Report database changes.
- Report tests performed.
- Show test results.
- Identify outstanding problems.
- State whether the phase is genuinely complete.
- Explain the next phase.

Do not automatically move into the next major phase without presenting the completed-phase report and obtaining the user's approval.

Small related tasks within an already approved phase can be completed together.

However, major architectural, database, financial or security decisions must be reviewed before implementation.

If a phase is incomplete, explain why and continue fixing it rather than claiming success.

 D. FIRST ACTION — INSPECT AND PLAN

Before writing substantial application code:

1. Inspect the available development environment.
2. Determine whether a project already exists.
3. Inspect existing files and configurations.
4. Confirm whether GitHub and Vercel are connected.
5. Confirm whether Supabase credentials and project configuration are available.
6. Identify missing credentials and integrations.
7. Never assume an account is connected simply because the user created it.
8. Never request secret API keys in ordinary chat messages.
9. Produce a project setup report.
10. Produce the initial implementation checklist.

If working in an existing repository, preserve useful existing work.

Do not overwrite or delete existing files without inspecting them first.

 E. DATABASE FIRST

Before implementing the complete application:

1. Review the proposed database entities.
2. Identify which entities are genuinely necessary.
3. Consolidate overlapping entities.
4. Produce a normalised relational schema.
5. Define table relationships.
6. Define primary and foreign keys.
7. Define constraints and indexes.
8. Define financial data types.
9. Define status values.
10. Define access policies.
11. Create version-controlled SQL migrations.
12. Configure Row Level Security.
13. Test access policies with different user roles.

Do not create all proposed tables blindly.

Create the tables needed for the approved current phase and the agreed architecture.

Avoid premature complexity while ensuring that foundational decisions do not prevent later features.

Present the proposed final schema and its relationships for review before applying major database migrations.

Never build the financial system around directly editable balance fields.

Use auditable financial ledger entries and atomic operations.

 F. IMPLEMENTATION APPROACH

Follow the development roadmap.

For each phase:

1. Explain the objective.
2. Identify dependencies.
3. Implement the feature.
4. Connect it to the database.
5. Apply permission checks.
6. Add input validation.
7. Add loading and error states.
8. Test the feature.
9. Fix identified defects.
10. Update technical documentation.
11. Report what has been completed.
12. Identify what remains.

Do not claim a feature is complete if it is only a visual interface.

A feature is complete only when its required frontend, backend, database, permissions and tests are implemented.

 G. USER INTERFACE REQUIREMENTS

Follow the MINAYO OPS design direction:

- Black.
- White.
- Cream.
- Dark Blue.
- Subtle Gold.
- Montserrat typography.

Create a premium, modern, clean and responsive interface.

Prioritise mobile usability.

Maintain consistent navigation and design patterns across all dashboards.

Do not make the interface unnecessarily crowded.

Build reusable components rather than duplicating interface code.

Design the public landing page early, but do not stop at the landing page.

Build the complete application according to the approved roadmap.

 H. SECURITY REQUIREMENTS

Security is a core feature, not a final decoration.

Implement:

- Authentication.
- Role-based access control.
- Row Level Security.
- Secure server-side operations.
- Protected administrative routes.
- Secure file access.
- Input validation.
- Rate limiting.
- Session management.
- Audit logging.
- Secure payment verification.
- Protection against unauthorised access.

Test each role independently.

A user must never access another user's private data by manipulating a URL or request.

 I. FINANCIAL REQUIREMENTS

Financial functionality requires special care.

Implement test-mode payment flows first.

Use verified payment events.

Use idempotency.

Record all financial changes.

Reconcile delayed or incomplete payment events.

Prevent duplicate refunds and payouts.

Maintain clear payment statuses.

Keep freelance commissions separate from marketplace commissions.

Respect the agreed rates:

- Freelance: 10%.
- Marketplace: 5%.

Do not activate live payment release until the required legal and technical fund-handling arrangement has been validated.

If the proposed Paystack workflow cannot safely support the requirements, document the limitation and recommend a compliant alternative.

Do not quietly change the platform's financial rules.

 J. AUTOMATION REQUIREMENTS

Implement reliable scheduled processing for:

- Contract review periods.
- Marketplace review periods.
- Job closing deadlines.
- Notifications.
- Payment reconciliation.
- Refund status tracking.
- Scheduled content.
- Reminders.

Scheduled operations must be safe to retry.

Prevent duplicate actions.

Maintain logs of automated activities.

Critical financial operations must be recoverable after failures.

 K. TESTING REQUIREMENTS

Write meaningful tests throughout development.

At minimum, test:

- Registration and login.
- Google authentication.
- User permissions.
- Job posting and applications.
- Interview invitations.
- Messaging.
- Offers.
- Contract acceptance.
- Contract funding states.
- Milestone approvals.
- Revisions.
- Deadline extensions.
- Automatic completion.
- Cancellation.
- Disputes.
- Refunds.
- Marketplace purchases.
- Marketplace delivery.
- Withdrawal requests.
- Commission calculations.
- Payment webhooks.
- Duplicate payment events.
- Administrative access.
- Data privacy.
- Mobile responsiveness.

Do not mark a phase complete until its required tests pass.

 L. GITHUB AND VERCEL

Use GitHub for version control.

Use meaningful commits.

Do not commit secrets, local environment files or private credentials.

Use Vercel for hosting.

Maintain separate development, staging and production environments.

Production deployment requires explicit Super Admin approval.

Never automatically deploy untested work to production.

 M. DOCUMENTATION

Maintain:

- README.md
- PRD.md
- TECHNICAL_HANDOVER.md
- DATABASE_SCHEMA.md
- DATABASE_RELATIONSHIPS.md
- SECURITY.md
- API_DOCUMENTATION.md
- PAYMENT_WORKFLOWS.md
- DEPLOYMENT_GUIDE.md
- TESTING_GUIDE.md
- ENVIRONMENT_VARIABLES.md
- DECISION_REGISTER.md
- DEVELOPMENT_PROGRESS.md

Update documentation as the application evolves.

Never put actual secret values inside documentation.

 N. COMMUNICATION AND WORK MANAGEMENT

Communicate clearly.

Do not overwhelm the user with unnecessary technical jargon.

Explain major architectural decisions in understandable language.

When an external service requires the user's action, explain exactly what needs to be done.

Do not claim that an account has been connected, an integration activated or a deployment completed unless it has actually been verified.

If a task cannot be completed because credentials, permissions or an external service are missing, explain the blocker and provide the next required action.

Do not repeatedly ask questions that have already been answered in the project documents.

Ask for clarification only when an important decision is genuinely missing or contradictory.

 O. SESSION CONTINUITY

Maintain an accurate development progress record.

At the end of each session, update:

- Current phase.
- Completed tasks.
- Incomplete tasks.
- Known defects.
- Database migration status.
- Integration status.
- Outstanding decisions.
- Next recommended action.

If a development session ends, the documentation and repository must make it possible to continue without restarting the project.

Never claim work was saved or committed unless it actually was.

 P. FINAL OBJECTIVE

Deliver a functional, secure, responsive and maintainable MINAYO OPS platform that follows the approved PRD and technical handover.

The platform must support real user accounts, real database operations, recruitment workflows, contracts, controlled financial records, marketplace functionality and administrative management.

Do not confuse a polished interface with a completed application.

Build the real product systematically.

 Q. YOUR FIRST RESPONSE

Do not immediately start generating the entire application.

First:

1. Confirm that you understand the project.
2. Summarise the architecture.
3. Inspect the available development environment.
4. Identify missing account connections and credentials without requesting secrets in chat.
5. Review the proposed database inventory.
6. Identify the minimum database entities required for the initial foundation.
7. Produce the initial implementation checklist.
8. Explain Phase 0.
9. Begin Phase 0 only after identifying the necessary setup requirements.

Do not jump directly into building every dashboard or feature.

Your first objective is to establish a correct, secure and maintainable foundation for MINAYO OPS.

END OF MASTER PROMPT.

---

 PART FOURTEEN — HOW TO USE THE DOCUMENT

 38. DEVELOPMENT HANDOVER

1. Save the approved PRD and this technical handover in the MINAYO OPS project folder.
2. Open the MINAYO OPS repository on GitHub.
3. Open Claude Code or another Claude environment capable of working with project files and a terminal.
4. Give Claude access to the PRD and this technical handover.
5. Paste the Master Prompt from Part Thirteen.
6. Let Claude inspect the environment and produce its setup report.
7. Review the proposed database schema before major migrations.
8. Allow Claude to implement Phase 0.
9. Review the completion report and approve the next phase.
10. Continue through the roadmap.

The documents are specifications, not evidence that external accounts are connected or that the platform has been deployed.

Claude must verify every integration.

FINAL DEVELOPMENT PRINCIPLE

Build the agreed product first, validate unresolved technical dependencies, test every phase and avoid unapproved features that increase complexity without serving the launch objectives.

The goal is a real, secure and maintainable MINAYO OPS—not merely a beautiful demo.
