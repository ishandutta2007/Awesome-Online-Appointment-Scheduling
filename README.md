# Awesome-Online-Appointment-Scheduling

# Awesome Online Appointment Scheduling

> A curated list of top Online Appointment Scheduling platforms — both SaaS/Hosted commercial solutions and open-source alternatives for letting customers self-book appointments, managing provider availability, and automating confirmations.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Calendly](#calendly)
  - [Acuity Scheduling](#acuity-scheduling)
  - [Zoho Bookings](#zoho-bookings)
  - [YouCanBookMe](#youcanbookme)
  - [SimplyBook.me](#simplybookme)
  - [Square Appointments](#square-appointments)
- [Open-Source Software](#-open-source-software)
  - [Easy!Appointments](#easyappointments)
  - [Cal.com](#calcom)
  - [Tymeslot](#tymeslot)
  - [Tidetime](#tidetime)
  - [Rallly](#rallly)
  - [Calnode](#calnode)
  - [Calrs](#calrs)
  - [justbookmycal](#justbookmycal)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Online Appointment Scheduling platforms. These are not open-source but are included as reference points for feature comparison.

### Calendly
**Type:** Meeting scheduling with self-service booking pages
Calendly popularized the self-service booking page model, allowing others to book time based on your availability without back-and-forth emails. It is the primary commercial reference for open-source alternatives like Easy!Appointments, Cal.com, and Tymeslot.

### Acuity Scheduling
**Type:** Appointment scheduling with intake forms and payments
Acuity (Squarespace) provides appointment scheduling with intake forms, payment processing, and automated reminders. It is positioned for service businesses (salons, tutors, consultants) wanting a polished, all-in-one booking experience.

### Zoho Bookings
**Type:** Appointment scheduling within Zoho ecosystem
Zoho Bookings provides scheduling pages, calendar sync, and payment collection as part of the broader Zoho suite. It is the natural choice for organizations already using Zoho CRM or other Zoho products.

### YouCanBookMe
**Type:** Booking pages with team scheduling
YouCanBookMe provides customizable booking pages with team scheduling, routing forms, and integrations with Google Calendar and Outlook. It is positioned for teams wanting flexible booking rules without a full platform.

### SimplyBook.me
**Type:** Appointment scheduling with plugins and marketplace
SimplyBook.me provides scheduling with a plugin marketplace, payment processing, and client management. It is positioned for SMBs wanting extensive customization through add-ons.

### Square Appointments
**Type:** Scheduling integrated with Square payments
Square Appointments provides scheduling, payment processing, and client management within the Square ecosystem. It is positioned for businesses already using Square for in-person payments.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Online Appointment Scheduling tools. The open-source ecosystem spans **mature GPL platforms with CMS integrations**, **modern TypeScript/Elixir booking systems**, **multi-provider company schedulers**, and **Doodle-style polling tools**.

### Easy!Appointments
**Stack:** PHP / MySQL | **License:** GPL-3.0
Easy!Appointments is the most established open-source appointment scheduler, in active development since 2014 with **220,000+ release downloads** and a **96% average satisfaction rating on Capterra** . Key features include:
- **Public booking page** where customers self-serve without creating accounts, plus an admin backend for managing providers, services, working hours, and appointments 
- **REST API and webhooks** for every booking, change, and cancellation, with SDKs for JavaScript, Python, PHP, and Ruby 
- **LDAP integration** so providers log in with existing credentials 
- **40+ languages** for the booking page and back office 
- **CMS integrations** for WordPress, Joomla, and Drupal, plus Docker deployment 
- **Google Calendar sync** and AI-agent accessibility through the same open API 

It is trusted by organizations including **Doctors Without Borders** and Germany's development ministry . **Trade-off:** It uses a PHP/MySQL stack with a web-based installation wizard rather than environment variables for initial setup .
**Best for:** Small to mid-sized businesses (clinics, salons, tutors, consultants) wanting a proven, feature-complete booking system with CMS integrations and no per-seat fees, accepting the PHP/MySQL deployment.

### Cal.com
**Stack:** TypeScript / Next.js / PostgreSQL / Prisma | **License:** AGPLv3 (open-core)
Cal.com is the most widely adopted open-source Calendly alternative, with a codebase that is open-source and self-hostable . It provides booking pages, team scheduling, calendar sync, video conferencing integration, and workflows. Deployment via Docker Compose with PostgreSQL and Traefik is documented, though the team notes Docker installations are supported by the user, not officially by Cal.com . **Important:** SMTP must be configured for booking confirmations, password resets, and team invitations to work; the app runs without email but those features are disabled . A managed cloud offering is also available.
**Best for:** Teams wanting a mature, feature-rich Calendly replacement with strong community adoption and the option to self-host or use the managed cloud.

### Tymeslot
**Stack:** Elixir / Phoenix LiveView / PostgreSQL | **License:** Open Source (self-hostable)
Tymeslot is an open-source, self-hostable alternative to Calendly and Cal.com, built with Elixir and Phoenix LiveView . Key features include:
- **Four booking themes** with custom colours and white-label options
- **Two-way calendar sync** with Google, Outlook, iCloud, and any CalDAV server (Nextcloud, Radicale, Zimbra, Baikal), with conflict checks across all calendars
- **Automatic video rooms** on Google Meet, Teams, Zoom, Jitsi, MiroTalk, kMeet, or Nextcloud Talk
- **Branded email templates** with `.ics` invites and no-login cancel/reschedule links
- **Webhooks** (HMAC-signed) for n8n, Zapier, and Make
- **Stripe Connect** optional paid bookings, fee-free for self-hosters

Self-hosting requires a single Docker container with PostgreSQL included. The same code powers both the self-hosted and managed cloud versions, with no gated features .
**Best for:** Teams wanting a modern, full-featured Calendly alternative with strong CalDAV support and a clean self-hosting story.

### Tidetime
**Stack:** Next.js 16 / React 19 / TypeScript / PostgreSQL / Drizzle | **License:** Open Source (self-hosted)
Tidetime is a self-hosted appointment scheduling system for a **single company with multiple services and multiple providers** . Key features include:
- **Services and providers** with per-service duration, location, intake questions, and optional manual confirmation
- **Provider assignment** where customers can choose a provider or let the system assign the least-busy available one, with bookings created inside a database transaction to prevent double-booking
- **Availability management** with per-provider weekly hours and named schedules
- **Calendar sync** with Google Calendar and Microsoft 365 for busy-time conflict checks, plus automatic Google Meet link generation
- **Webhooks** (signed, Zapier-compatible) for booking events
- **Branding and custom domain** with automatic HTTPS certificate renewal

Deploys via Docker and Caddy. There is no hosted plan, no per-seat pricing, and no third-party analytics .
**Best for:** Small companies wanting a self-hosted, multi-provider booking system with strong calendar sync and no SaaS dependency, accepting the Next.js/PostgreSQL deployment.

### Rallly
**Stack:** Next.js / Prisma / tRPC / TypeScript / PostgreSQL | **License:** Open Source
Rallly is an open-source **meeting poll and group scheduling** tool, explicitly positioned as a Doodle alternative . Key features include:
- **No-account voting** — participants vote on proposed times without signing up 
- **Multi-language support** (10+ languages) 
- **Custom branding** via environment variables 
- **Magic-link authentication** and SSO support (Google, Microsoft Entra ID, OIDC) 
- **ICS calendar files** emailed with finalized meetings 
- **Admin control panel** for managing users and settings 

Deployment via Railway or Docker with PostgreSQL and MinIO for object storage. Hardware requirements are modest: 1 vCPU / 2 GB RAM minimum, 2 vCPU / 4 GB recommended . **Important distinction:** Rallly is a polling tool for finding a time that works for a group, not a Calendly-style self-booking page.
**Best for:** Teams needing Doodle-style group availability polling without accounts, accepting the polling rather than self-booking model.

### Calnode
**Stack:** Go / SQLite | **License:** Apache-2.0
Calnode is a lean, self-hostable scheduling engine built as a **single Go binary with SQLite**, positioned as a Calendly/Cal.com alternative . Key features include:
- **API-first and MCP-native**: a Model Context Protocol server is compiled into the binary, exposing tools like `get_available_slots`, `create_booking`, and `reschedule_booking`
- **OAuth 2.1 authorization server** for agent connections, plus API keys for scripts
- **HMAC-signed webhooks** for booking lifecycle events
- **Conversational booking** on the booking page, with the deterministic engine computing slots (the model never invents times)
- **Google/Microsoft calendar sync** and meeting link generation

It is positioned for teams wanting a small, fast, scriptable, and AI-ready scheduler .
**Best for:** Developers and AI-forward teams wanting a lightweight, MCP-native scheduling engine with a single binary and no heavy dependencies.

### Calrs
**Stack:** Rust | **License:** Open Source
Calrs is a fast, self-hostable scheduling platform written in Rust, positioned as a Cal.com alternative . Key features include:
- **Team scheduling** with round-robin (least-busy assignment) or collective (all members must be free) modes
- **Unified Teams** created from OIDC groups or hand-picked users, with public or private visibility
- **Invite links** with tokenized access, expiration, and usage limits for internal or private event types
- **CalDAV calendar sync** for conflict checks, with multi-timezone team support
- **Availability overrides** for specific dates or custom hours

It uses local accounts with Argon2 hashing and supports OIDC/SSO via Keycloak or Authentik .
**Best for:** Teams wanting a Rust-based, performance-focused scheduling platform with strong team and invite-link features, accepting a newer ecosystem.

### justbookmycal
**Stack:** Python / Flask | **License:** Open Source (PyPI)
justbookmycal is a lightweight, self-hosted booking page that checks your live calendar via **ICS feeds** . Key characteristics:
- **ICS feed-based availability**: reads busy times from any published ICS feed, treating `TRANSP:TRANSPARENT` and `CANCELLED` events as free
- **Cache with fallback**: caches feeds and uses the last copy (up to 24 hours old) if a feed cannot be loaded, rather than risking double booking
- **Email invitations** with `.ics` attachments, using a system address as organizer
- **Private links** for each side, derived from `SECRET_KEY`, with only hashes stored in the database
- **Jitsi video links** by default, with configurable templates

It is designed for a single person's booking page rather than team scheduling .
**Best for:** Individuals wanting a minimal, self-hosted booking page that works with any ICS feed, accepting a narrower feature set than full platforms.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Multi-Provider | Calendar Sync | Self-Hosted | Best For |
|----------|---------|-------|----------------|---------------|-------------|----------|
| **Calendly** | Proprietary | Cloud | ✅ | ✅ | ❌ | Standard booking pages |
| **Acuity** | Proprietary | Cloud | ✅ | ✅ | ❌ | Service business + payments |
| **Easy!Appointments** | GPL-3.0 | PHP/MySQL | ✅ | ✅ Google | ✅ | Proven CMS-integrated scheduler |
| **Cal.com** | AGPLv3 | Next.js/Postgres | ✅ | ✅ | ✅ | Mature Calendly alternative |
| **Tymeslot** | Open Source | Elixir/Phoenix | (Check) | ✅ Any CalDAV | ✅ | Full-featured + CalDAV |
| **Tidetime** | Open Source | Next.js/Postgres | ✅ | ✅ Google/M365 | ✅ | Multi-provider company |
| **Rallly** | Open Source | Next.js/Prisma | (Polling) | (ICS final) | ✅ | Doodle-style group polls |
| **Calnode** | Apache-2.0 | Go/SQLite | (Check) | ✅ Google/M365 | ✅ | AI-agent bookable |
| **Calrs** | Open Source | Rust | ✅ Team modes | ✅ CalDAV | ✅ | Rust team scheduling |
| **justbookmycal** | Open Source | Python/Flask | ❌ (Single) | ✅ ICS feeds | ✅ | Minimal ICS-based page |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Online Appointment Scheduling tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

**Note on the open-source ecosystem:** The appointment scheduling space splits between **full booking platforms** (Easy!Appointments for maturity and CMS integrations, Cal.com for the largest community, Tymeslot for feature depth with CalDAV, Tidetime for multi-provider companies, Calrs for Rust-based team scheduling) and **group polling tools** (Rallly for Doodle-style availability finding). **Easy!Appointments** is the most proven open-source scheduler, with 12 years of development, 220k+ downloads, and use by Doctors Without Borders . **Cal.com** remains the most widely adopted Calendly alternative with the largest community . For teams wanting AI-agent accessibility, **Calnode** uniquely compiles an MCP server into its binary, allowing agents to book meetings directly . **Rallly** fills the distinct need for group availability polling rather than self-booking. No open-source project fully replicates Calendly's ecosystem polish, but these tools cover the core booking workflow comprehensively for self-hosted deployments.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
