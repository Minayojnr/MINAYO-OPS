MINAYO OPS
PRODUCT REQUIREMENTS DOCUMENT (PRD)
Version 1.0 | October 2026
Product: MINAYO OPS
Initial Market: Nigeria
Primary Currency: Nigerian Naira (₦)
Primary Language: English
Document Status: Product specification for development planning
1. PRODUCT OVERVIEW
1.1 Introduction
MINAYO OPS is a Nigeria-first digital platform designed to connect people and organisations with work opportunities, freelance talent, digital products and services.
The platform allows clients to publish work opportunities and hire freelancers. Freelancers can discover opportunities, submit applications, communicate with clients, negotiate contracts and earn money by providing services.
The platform also includes a marketplace where users can buy and sell eligible digital products and services.
1.2 Product Vision
To make it easier for people to discover opportunities, connect with the right people, create value and earn through a trusted digital platform.
1.3 Product Goals
•	Provide a straightforward way for clients to publish work and hire suitable talent.
•	Help freelancers discover opportunities and manage applications, contracts and earnings.
•	Support transparent agreements, revisions, deadlines and dispute resolution.
•	Provide a marketplace for digital products and services.
•	Give administrators the tools to operate, moderate and monitor the platform.
•	Launch with a secure, manageable and cost-conscious technology foundation that can grow over time.
1.4 Out of Scope for Initial Launch
The following features are not included in the initial launch:
•	Native Android and iOS applications.
•	Voice and video calls.
•	Interview scheduling.
•	Public challenges.
•	Public platform statistics.
•	Multiple currencies.
•	Multiple interface languages.
•	Cash referral rewards.
•	Promotional discount campaigns.
•	Blog comments.
•	Newsletter subscriptions.
The initial platform should be mobile-responsive and Progressive Web App (PWA) capable.
2. USERS, ACCOUNT TYPES AND ROLES
MINAYO OPS will have two ordinary account types:
1.	Client
2.	Freelancer
Administrative roles will be separate from ordinary user accounts.
2.1 Visitor
A visitor is someone who accesses the platform without registering.
Visitors can:
•	View the landing page.
•	Read About Us and Contact Us pages.
•	View permitted public freelancer profiles.
•	Browse public marketplace listings.
•	Preview available job opportunities.
•	Read blog posts and announcements where publicly available.
Visitors must register or sign in before submitting a job application.
2.2 Client
A client is a person or organisation that brings work opportunities to the platform and hires freelancers.
Clients can:
•	Create and publish job opportunities.
•	View and manage their job postings.
•	Review freelancer applications.
•	Shortlist applicants.
•	Invite freelancers for interviews.
•	Compare applicants and their proposed rates.
•	Communicate with freelancers.
•	Negotiate prices.
•	Send contract offers.
•	Manage contracts.
•	Fund contracts.
•	Approve completed work.
•	Request revisions.
•	Report contract problems.
•	Review freelancers.
•	Buy products and services from the marketplace.
2.3 Freelancer
A freelancer is a user who discovers opportunities and provides services in exchange for payment.
Freelancers can:
•	Create and manage their profiles.
•	Browse available jobs.
•	Apply for opportunities.
•	Bookmark jobs.
•	Track applications.
•	Accept or reject interview invitations.
•	Communicate with clients.
•	Negotiate contract terms.
•	Accept or decline offers.
•	Manage contracts.
•	Submit completed work.
•	Request deadline extensions.
•	Request payment withdrawals.
•	Sell eligible products or services.
•	Purchase marketplace products.
•	Review clients after eligible completed contracts.
2.4 Administrative Roles
The platform will support the following administrative roles:
Role	Responsibility
Super Admin	Full platform control and ownership-level access
Admin	General platform operations
Moderator	User reports, content and listing moderation
Support Staff	Customer support and ticket management
Finance Staff	Transactions, refunds, withdrawals and financial monitoring
Important: Only the Super Admin can view the platform audit log.
3. REGISTRATION AND AUTHENTICATION
3.1 Registration
Users must select their account type during registration:
•	Client
•	Freelancer
Google sign-in must be supported alongside the standard authentication method.
3.2 Profile Setup
Freelancers should complete their profiles during registration.
Profile information may include:
•	Full name.
•	Profile picture.
•	Professional title.
•	Location.
•	Skills.
•	Experience.
•	Education or relevant qualifications.
•	Portfolio.
•	Professional description.
•	Relevant service information.
Profile completion should be displayed as a percentage.
Incomplete profiles must not automatically prevent freelancers from applying for opportunities.
Instead, the platform should display a notice explaining that completing their profile may improve their chances of being hired.
Some profile information may remain optional.
3.3 Identity Verification
Identity verification will be optional initially.
Supported identity documents may include:
•	National Identification Number (NIN).
•	Driver's licence.
•	International passport.
Verification statuses:
•	Not Verified.
•	Pending.
•	Verified.
•	Rejected.
If verification is rejected, the user should receive an appropriate explanation and an option to resubmit.
Automated verification is preferred, with an administrative fallback where automated verification is unsuccessful or inconclusive.
The verification provider must be selected before this feature is enabled.
3.4 Account Security
The platform should support:
•	Secure password handling.
•	Password recovery.
•	Optional two-factor authentication for ordinary users.
•	Mandatory two-factor authentication for Super Admin.
•	Login activity monitoring.
•	Account deactivation and deletion requests.
•	Personal data export requests.
•	Automatic logout after a defined period of inactivity.
Age is user-entered. The platform should not unnecessarily exclude young skilled users, but must apply legally required safeguards for minors.
4. PUBLIC WEBSITE
The landing page should be the first major point of interaction.
It should introduce MINAYO OPS, explain its purpose and direct visitors towards registration or sign-in.
Public pages should include:
•	Landing Page.
•	About Us.
•	Contact Us.
•	Blog/News.
•	Public Freelancer Profiles.
•	Public Marketplace Listings.
•	Opportunity Previews.
Visitors should be able to see permitted public content without creating an account.
Private dashboards, messages, contracts and personal records must never be publicly indexed.
The blog should be read-only, without comments or newsletter subscriptions.
Official social media links should be manageable by administrators.
5. FREELANCER DASHBOARD
5.1 Main Navigation
The freelancer dashboard should contain four main sections:
1.	Find Work
2.	My Contracts
3.	Messages
4.	Marketplace
5.2 Hamburger Menu
The freelancer hamburger menu should contain:
•	My Profile.
•	Wallet.
•	About.
•	Support.
5.3 Find Work
Freelancers should be able to:
•	Browse available opportunities.
•	Search for jobs.
•	Filter opportunities.
•	View job descriptions.
•	View client requirements.
•	View budgets or proposed rates.
•	Apply for opportunities.
•	Bookmark opportunities.
There should be no fixed application limit at launch.
5.4 Applications
Freelancers should be able to monitor their application progress.
Application statuses:
1.	Submitted.
2.	Under Review.
3.	Shortlisted.
4.	Interview.
5.	Offer Received.
6.	Hired.
7.	Rejected.
8.	Withdrawn.
Freelancers may withdraw applications before hiring.
Withdrawn applications should remain in their application history.
5.5 My Contracts
This section should provide access to contracts and relevant application tracking.
Freelancers should be able to view:
•	Active contracts.
•	Completed contracts.
•	Cancelled contracts.
•	Contract details.
•	Deliverables.
•	Deadlines.
•	Revision allowances.
•	Payment status.
5.6 Messages
The messaging section should support text-based communication between clients and freelancers.
Voice calls and video calls are not included at launch.
5.7 Marketplace
Freelancers should be able to browse marketplace products and services.
Those who meet the seller requirements should also be able to create listings.
6. CLIENT DASHBOARD
6.1 Main Navigation
The client dashboard should contain:
1.	Post Work.
2.	Hire Talent.
3.	Contracts.
4.	Messages.
5.	Marketplace.
6.2 Hamburger Menu
The client hamburger menu should mirror the freelancer menu:
•	My Profile.
•	Wallet.
•	About.
•	Support.
6.3 Posting Work
Clients should be able to create opportunities containing:
•	Job title.
•	Job description.
•	Category.
•	Required skills.
•	Budget or rate.
•	Work arrangement.
•	Requirements.
•	Deadline.
•	Deliverables.
•	Other relevant contract terms.
Supported work arrangements should include:
•	Full-time.
•	Remote.
•	On-site.
•	Other suitable work arrangements.
The platform owner and authorised administrators should also be able to publish job opportunities.
6.4 Job Management
Clients should be able to:
•	View published jobs.
•	View applications.
•	Shortlist applicants.
•	Reject applicants.
•	Invite freelancers to apply.
•	Compare applicants.
•	Close job postings.
Clients do not need manual administrative approval before ordinary job postings go live.
Automated monitoring should identify suspicious or potentially prohibited listings for review.
Once applications have started, clients should not be allowed to change the core terms of the opportunity.
Instead, they should close the existing job and create a new posting.
This prevents applicants from being disadvantaged by changes to previously published terms.
Jobs should automatically close when their deadlines expire and move into job history.
6.5 Job Categories
The initial categories should include:
1.	Graphics & Design.
2.	Writing & Translation.
3.	Programming & Technology.
4.	Video & Animation.
5.	Digital Marketing.
6.	Business & Finance.
7.	AI Services.
8.	Data & Research.
9.	Administrative Support.
10.	Engineering & Architecture.
7. INTERVIEWS AND MESSAGING
7.1 Interview Invitations
Clients should be able to invite shortlisted freelancers for interviews.
When an invitation is sent:
•	The freelancer receives an immediate notification or popup.
•	The freelancer can accept or reject.
•	Accepting the invitation opens a text-based chat.
•	Rejecting the invitation updates the interview status.
There will be no interview scheduling feature at launch.
7.2 Messaging
Clients and freelancers should communicate through the platform.
Messaging should support:
•	Text messages.
•	Relevant file attachments.
•	Message history.
•	Notifications for new messages.
•	Reporting inappropriate messages or behaviour.
Users should be able to block other users.
Blocking should prevent new conversations but must not erase existing contracts or financial obligations.
8. OFFERS AND CONTRACT CREATION
8.1 Negotiation
Clients and freelancers should negotiate prices and contract terms through messaging.
Offers may be:
•	Accepted.
•	Declined.
•	Returned for changes.
8.2 Contract Generation
Once both parties agree on the final terms:
1.	The client sends the final offer.
2.	The freelancer accepts.
3.	The platform generates the contract automatically.
4.	Both parties review the contract.
5.	Both parties digitally accept it.
6.	The contract becomes active.
The contract should contain:
•	Client details.
•	Freelancer details.
•	Scope of work.
•	Deliverables.
•	Agreed price.
•	Payment structure.
•	Deadlines.
•	Revision allowance.
•	Other agreed conditions.
The contract becomes active before the payment step, but work cannot begin until the required funds are confirmed as secured.
9. CONTRACT MANAGEMENT AND DELIVERY
9.1 Funding
Clients must fund the full contract amount upfront through the platform's approved payment arrangement.
For milestone contracts, the total contract amount should be funded and allocated across the milestones.
9.2 Revisions
The number of included revisions must be agreed before work begins and stated in the contract.
Additional revisions require negotiation of an additional fee.
The client must accept the additional fee before the extra work becomes part of the agreement.
9.3 Deadline Extensions
Freelancers may request deadline extensions.
The client must approve the request.
Both parties may also mutually agree to extend deadlines.
All approved changes must be recorded in the contract.
9.4 Work Submission
Freelancers should be able to submit completed work and supporting files through the contract workspace.
9.5 Completion
The client may:
•	Approve the completed work.
•	Request revisions.
•	Report a problem.
When the client clicks Contract Completed, the system should initiate the agreed payout process.
9.6 Seven-Day Pending Period
If a freelancer submits final work and the client does not respond, a seven-day pending review period should apply before automatic completion and payout.
During this period, the client may:
•	Approve the work.
•	Request revisions.
•	Report a problem.
The platform should send reminders and display the deadline clearly.
If a problem is reported, the funds should remain on hold for review.
10. CANCELLATIONS AND DISPUTES
Either party may request contract cancellation.
10.1 Cancellation Before Work Begins
If cancellation is approved before work begins, the client should receive a full refund.
10.2 Cancellation After Work Begins
If work has started, an authorised Admin should determine a fair refund based on:
•	Contract terms.
•	Work completed.
•	Evidence submitted.
•	Circumstances of the cancellation.
10.3 Dispute Resolution
An active contract should have a Report a Problem option.
When a dispute is raised:
•	The disputed funds remain on hold.
•	Both parties may submit evidence.
•	Admin reviews relevant contract terms, messages and submissions.
•	Admin makes a decision based on the available evidence.
•	Both parties receive the outcome.
•	An appeal route should be available.
Evidence may include:
•	Messages.
•	Files.
•	Screenshots.
•	Submitted deliverables.
•	Contract terms.
The target resolution period should be 5–7 working days, depending on the complexity of the case.
Contracts and receipts should be downloadable.
11. PAYMENTS AND WALLETS
11.1 Platform Commission
The platform's commission structure is:
Transaction	Commission
Freelance contracts	10%
Marketplace sales	5%
Changes to commission rates should apply only to new transactions.
Existing accepted contracts must not be affected retroactively.
Applicable fees must be displayed before users confirm transactions.
11.2 Client Wallet
Clients should be able to:
•	Fund their wallets.
•	Fund contracts.
•	View transaction history.
•	View available balances.
•	Withdraw unused eligible funds.
11.3 Freelancer Wallet
Freelancers should be able to:
•	View available earnings.
•	View pending earnings.
•	View transaction history.
•	Request withdrawals.
•	Manage bank details.
Freelancers should be able to withdraw all available eligible balances.
There should be no minimum withdrawal threshold at launch.
11.4 Withdrawals
The platform should:
•	Validate bank account details.
•	Verify bank-account ownership.
•	Process eligible withdrawals automatically.
•	Allow authorised Finance/Admin staff to hold or reject suspicious withdrawals.
11.5 Financial Records
The system must maintain a proper financial ledger.
Balances must be derived from recorded transactions rather than relying on manually editable balance fields.
Users should have access to:
•	Transaction history.
•	Wallet statements.
•	Receipts.
•	Applicable invoices.
Administrators should be able to generate financial reports covering:
•	Revenue.
•	Commissions.
•	Refunds.
•	Withdrawals.
•	Transactions.
Reports should be exportable to Excel and PDF.
11.6 Payment Gateway
Paystack is the preferred initial payment gateway.
However, the platform must be designed so another payment provider can be integrated if necessary.
All payment operations should support:
•	Verified payment events.
•	Idempotency.
•	Transaction reconciliation.
•	Failed-payment handling.
•	Delayed-payment handling.
•	Refund processing.
•	User notifications.
Important production requirement: Do not assume that an ordinary Paystack merchant account supports legally compliant escrow, custodial holding or delayed fund release. The exact payment arrangement must be validated against Nigerian legal and regulatory requirements and confirmed with the payment provider before enabling live contract fund holding and automated payouts.
Until this is validated, the relevant financial workflow should remain in test mode or disabled.
If a payment becomes stuck or cannot be completed, the platform must reconcile it, notify affected users and initiate the appropriate refund process rather than leaving the money unresolved.
12. MARKETPLACE
The marketplace should support digital products and services.
12.1 Seller Listings
Sellers should be able to publish:
•	Digital products.
•	Creative services.
•	Other eligible digital services.
Listings should contain:
•	Product or service title.
•	Description.
•	Category.
•	Price.
•	Delivery timeline.
•	Usage rights.
•	Relevant images or files.
•	Revision allowance where applicable.
12.2 Usage Rights
Sellers should specify applicable usage rights:
•	Personal use.
•	Commercial use.
•	Extended usage rights.
Where technically and commercially appropriate, buyer-specific watermarks or identifying details should be applied.
12.3 Listing Approval
New marketplace listings require Admin approval.
Significant listing edits may require another review.
Administrators should be able to hide or remove listings that violate platform policies.
12.4 Marketplace Discovery
Buyers should be able to search and filter listings by:
•	Price.
•	Category.
•	Rating.
•	Popularity.
•	Relevance.
Sorting should support:
•	Newest.
•	Price.
•	Ratings.
•	Relevance.
Personalised recommendations should also be supported.
12.5 Purchases and Delivery
Buyers should have access to their purchase history.
Eligible digital products should be available for re-download.
Sellers should specify delivery timelines.
Buyers may request revisions within the allowance stated in the listing.
Sellers may reject unreasonable requests that fall outside the listing terms.
12.6 Seven-Day Inspection Period
Buyers should have seven days after delivery to inspect their purchase.
The platform should send reminders.
If a buyer reports a problem, the funds should remain on hold for review.
If the buyer does not respond, the order should be referred to Admin before funds are released.
The exact payment-release rule after revised delivery must be finalised before the marketplace payment system goes live.
13. RATINGS AND REVIEWS
Clients and freelancers should be able to review one another after a verified completed contract.
Reviews should include:
•	A 1–5 star rating.
•	An optional written comment.
Reviews should appear publicly on the relevant profiles.
Users should be allowed to respond publicly to reviews.
Users should be able to report fake, abusive or misleading reviews.
Administrators should be able to moderate reported reviews.
Marketplace reviews must be linked to eligible purchases.
14. NOTIFICATIONS
The platform should support in-app notifications and appropriate email or push notifications.
Important notification events include:
•	New messages.
•	Application updates.
•	Interview invitations.
•	Offers.
•	Contract updates.
•	Deadline reminders.
•	Payment confirmations.
•	Withdrawal updates.
•	Dispute updates.
•	Support replies.
Users should be able to mark notifications as read.
Announcements should remain in notification history.
Users should control notification preferences by category and channel.
Critical security emails should remain enabled.
15. SUPPORT SYSTEM
The platform should provide:
•	Help Centre.
•	FAQs.
•	Contact Us form.
•	Official support email.
•	Support tickets.
•	Ticket assignment.
•	Support replies.
•	Ticket status notifications.
Users should receive confirmation after submitting a support request.
Administrators should be able to assign and manage support tickets.
Support operating hours and expected response times should be displayed once established.
16. ADMINISTRATION
16.1 Super Admin
The Super Admin should have full control over the platform.
This includes:
•	User management.
•	Administrative roles.
•	Platform settings.
•	Financial oversight.
•	Commission settings.
•	Content management.
•	Moderation oversight.
•	Maintenance mode.
•	Appearance editor.
•	Production-level configuration.
Only the Super Admin should be able to view the audit log.
16.2 Admin
Admins should manage normal platform operations within their assigned permissions.
16.3 Moderator
Moderators should manage:
•	User reports.
•	Suspicious content.
•	Marketplace listing reports.
•	Policy violations.
16.4 Support Staff
Support Staff should manage customer support tickets and related user enquiries.
16.5 Finance Staff
Finance Staff should monitor:
•	Transactions.
•	Refunds.
•	Withdrawals.
•	Reconciliation.
•	Financial reports.
16.6 Administrative Content Management
Administrators should be able to:
•	Draft blog posts.
•	Preview blog posts.
•	Schedule blog posts.
•	Publish announcements.
•	Schedule announcements.
•	Archive old content.
•	Publish platform-owned job opportunities.
17. DESIGN AND USER EXPERIENCE
17.1 Brand Identity
The platform should use the following design direction:
Element	Requirement
Primary colours	Black and white
Supporting colours	Cream and dark blue
Accent	Subtle gold
Font	Montserrat
Style	Modern, premium and clean
Layout	Mobile-first and responsive
17.2 Appearance Editor
The Super Admin should have access to a platform appearance editor.
The editor should allow changes to:
•	Colours.
•	Fonts.
•	Light mode.
•	Dark mode.
Changes should be saved and reflected across the website.
Users should also be able to select their preferred light or dark mode.
17.3 Accessibility
The interface should support:
•	Readable text.
•	Appropriate colour contrast.
•	Keyboard accessibility.
•	Clear labels.
•	Scalable text.
•	Responsive layouts.
•	Clear success and error messages.
18. ADDITIONAL PLATFORM FEATURES
The platform should also support:
•	Bookmarked jobs.
•	Bookmarked freelancers.
•	Bookmarked marketplace items.
•	Guided onboarding with a skip option.
•	Referral codes and referral links.
•	Cookie consent controls.
•	Automatic timezone detection.
•	User-selectable date formats.
•	Standard Naira currency formatting.
•	Progressive Web App support.
•	Basic SEO for public pages.
•	Official social media link management.
Referral rewards should not involve cash at launch.
Recently viewed history is not required.
19. SECURITY, PRIVACY AND USER SAFETY
The platform should include:
•	Encryption in transit and at rest where supported.
•	Secure authentication.
•	Role-based permissions.
•	Database-level access controls.
•	Private storage for identity documents.
•	Secure handling of financial records.
•	Suspicious activity monitoring.
•	User reporting and blocking.
•	Temporary restrictions pending Admin review.
•	Appeals for enforcement decisions.
•	Automatic session logout after inactivity.
•	Daily database backups.
•	Documented recovery procedures.
The platform should also publish:
1.	Prohibited Activities and Services Policy.
2.	Fair Usage Policy.
3.	Dispute Resolution Policy.
4.	User Code of Conduct.
Significant policy changes should require notification and acceptance.
Data retention and deletion must follow applicable legal requirements.
20. TECHNICAL REQUIREMENTS
The proposed initial technology stack is:
Technology	Purpose
Next.js	Frontend and application framework
TypeScript	Application programming language
Tailwind CSS	Interface styling
Supabase	Database, authentication and storage
PostgreSQL	Relational database
Vercel	Hosting and deployment
GitHub	Source code management
Paystack	Payment gateway
Resend	Transactional email
Termii	SMS and OTP
Sentry	Error monitoring
PostHog	Product analytics
The platform should initially use a modular monolithic architecture rather than unnecessary microservices.
Development should use separate environments:
•	Development.
•	Staging.
•	Production.
All secrets must be stored securely in environment variables.
The project should use GitHub version control.
Database backups and restoration procedures must be documented.
21. SUCCESS METRICS
The platform should internally track:
•	Visitor-to-registration conversion.
•	Client registration completion.
•	Freelancer registration completion.
•	Freelancer profile completion.
•	Jobs posted.
•	Applications received.
•	Application-to-interview conversion.
•	Interview-to-hire conversion.
•	Contracts created.
•	Contracts completed.
•	Contract dispute rate.
•	Payment success rate.
•	Payment failure rate.
•	Refund rate.
•	Marketplace purchases.
•	Marketplace dispute rate.
•	Support ticket volume.
•	User retention.
•	Repeat client activity.
These statistics are for internal monitoring. Public platform statistics are not required at launch.
22. DEVELOPMENT PHASES
MINAYO OPS should be developed gradually.
The platform must not be built all at once.
Phase	Development Focus
Phase 0	Project setup and environment inspection
Phase 1	Database, authentication and security foundation
Phase 2	Brand system, public website and dashboard UI
Phase 3	Profiles, jobs and recruitment
Phase 4	Messaging, interviews and offers
Phase 5	Contracts and work delivery
Phase 6	Wallets, payments and financial system
Phase 7	Marketplace
Phase 8	Admin, support and notifications
Phase 9	Security, testing and quality assurance
Phase 10	Beta testing and public launch
Each phase must be completed, tested and documented before moving to the next major phase.
The product owner must review and approve each major phase.
The development team must inspect the existing repository and environment before making changes.
Existing working code must not be overwritten unnecessarily.
23. OPEN DECISIONS AND ITEMS REQUIRING VALIDATION
The following matters must be resolved before the relevant features go live:
1.	Nigerian legal and regulatory validation of the contract fund-holding and payout arrangement.
2.	Selection of an identity verification provider.
3.	Final marketplace payment-release rule after revised delivery.
4.	Responsibility for gateway charges on refunds.
5.	Automatic logout duration.
6.	Support operating hours and response targets.
7.	Data retention periods.
8.	Minor safeguards and consent requirements.
9.	Dispute appeal deadlines.
10.	Payment reconciliation intervals and escalation process.
11.	Hosting, storage, email, SMS and monitoring budgets.
These items should be tracked rather than guessed.
24. ACCEPTANCE CRITERIA
A feature should not be considered complete merely because its interface has been created.
Before a feature is accepted:
•	Its main workflow must function correctly.
•	Its permissions must be tested.
•	Its error states must be handled.
•	Its data must be stored and retrieved correctly.
•	Relevant security rules must be tested.
•	Important edge cases must be covered.
•	Documentation must be updated.
Financial workflows must be tested using successful, failed, delayed and repeated payment events.
No integration, account connection, payment flow or deployment should be described as successful until it has been verified.
The product owner must approve each major development phase.
25. CORE USER JOURNEYS
25.1 Client Hires a Freelancer
1.	Client registers or signs in.
2.	Client completes account setup.
3.	Client publishes a work opportunity.
4.	Freelancers discover and apply.
5.	Client reviews and compares applicants.
6.	Client shortlists or invites a freelancer for an interview.
7.	Freelancer accepts the interview invitation.
8.	Text chat opens.
9.	Both parties negotiate the contract.
10.	Client sends the final offer.
11.	Freelancer accepts.
12.	The platform generates the contract.
13.	Both parties digitally accept the contract.
14.	Client funds the contract through the approved payment arrangement.
15.	Work begins once funds are confirmed as secured.
16.	Freelancer submits the work.
17.	Client approves, requests revisions or reports a problem.
18.	The payment process proceeds according to the validated contract and financial rules.
25.2 Freelancer Applies for Work
1.	Freelancer signs in.
2.	Freelancer opens Find Work.
3.	Freelancer searches or filters opportunities.
4.	Freelancer opens a job.
5.	Freelancer reviews the requirements.
6.	Freelancer submits an application.
7.	Application appears in the freelancer's tracking area.
8.	Freelancer receives status updates.
9.	Freelancer may withdraw before hiring.
10.	If invited to interview, the freelancer receives a notification and responds.
25.3 Marketplace Purchase
1.	Buyer opens the marketplace.
2.	Buyer searches or browses approved listings.
3.	Buyer reviews the description, price, usage rights and delivery terms.
4.	Buyer makes a purchase through the approved payment flow.
5.	Seller delivers the product or service.
6.	Buyer inspects the delivery within seven days.
7.	Buyer may request permitted revisions or report an issue.
8.	The order proceeds under the final approved payment-release rule.
26. CONCLUSION
MINAYO OPS is intended to become a platform where people can discover opportunities, connect with talent, create value and earn.
Its foundation rests on five major areas:
1.	Opportunities: Helping people discover and apply for work.
2.	Talent: Connecting clients with suitable freelancers.
3.	Contracts: Providing structured agreements and work management.
4.	Payments: Supporting transparent and accountable financial transactions.
5.	Marketplace: Enabling the buying and selling of digital products and services.

