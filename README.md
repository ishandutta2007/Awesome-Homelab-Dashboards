# Awesome-Homelab-Dashboards

## Top Homelab Dashboards Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Service Launchers, Live Status Widgets & Self-Hosted Start Pages*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Homelab Dashboards**. These tools provide a single landing page for your self-hosted services—organizing links, displaying live status from media servers and monitoring tools, and replacing the scattered bookmarks and half-remembered IP addresses that accumulate in every homelab.



**Examples** include Heimdall, Homer, Flame, Dashy, Homarr, Organizr, Glance, and Homepage (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, avoiding vendor lock-in, and running a dashboard on minimal hardware—ideal for homelab enthusiasts, self-hosters, and anyone who wants a fast, private start page without cloud dependency. The open-source landscape is anchored by **Heimdall** (the beginner-friendly drag-and-drop launcher), **Homarr** (the Plex/*arr integration specialist), **Dashy** (the customization maximalist), and **Flame** (the minimalist search-first start page), with **Homepage** offering the deepest service integrations and **Homer** providing the simplest static YAML option.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## Sector Overview & Market Dynamics

The broader cloud Platform-as-a-Service (PaaS) and developer hosting market is valued at approximately **$90B–$140B** (projected to exceed $350B by 2030 at ~18–20% CAGR), while specialized managed open-source homelab/app hosting represents a rapidly growing sub-niche of several hundred million dollars. The sector is **moderately fragmented**: core cloud compute is anchored by hyper-scalers (AWS, Azure, GCP), but the application-layer deployment and self-hosted tooling space exhibits a competitive, highly fragmented ecosystem of specialized PaaS providers and managed container hosts.

## SaaS/Hosted Platforms

While homelab dashboards are fundamentally designed to run on local private networks to connect to local devices and containers, several managed cloud hosting platforms and specialized SaaS solutions provide turn-key environments for deploying and monitoring homelab dashboards without local bare-metal hardware.

| Platform | Starting Pricing | Free Tier / Trial Limits | Company Size (Valuation / Revenue) | Description |
| :--- | :--- | :--- | :--- | :--- |
| **[Render](https://render.com)** | $7/month (Starter compute tier; Pro workspace at $25/month) | 750 free instance hours/month; web services spin down after 15 minutes of inactivity; free PostgreSQL expires after 30 days (1 GB cap) | ~$1.5B Valuation ($27M ARR run-rate) | Unified cloud application platform offering Git-automated builds, persistent services, and managed databases to run containerized dashboards. |
| **[Railway](https://railway.com)** | $5/month (Hobby plan base price, includes $5 usage credits) | 30-day free trial ($5 one-time credit, capped at 2 vCPU / 1 GB RAM / 0.5 GB volume); reverts to $1/month usage credit free tier (0.5 GB RAM, 1 vCPU) | ~$500M–$1B Est. Valuation (~$10M–$30M ARR, $120M raised) | Cloud infrastructure orchestration platform enabling 1-click template and repository deployments for homelab startpages and utility apps. |
| **[Netdata Cloud](https://www.netdata.cloud)** | $4.50/node/month (billed annually) or $90/year Homelab plan | Free Forever Community plan for up to 5 active nodes; unlimited per-second metrics and real-time interactive monitoring dashboards | ~$68M–$85M Est. Valuation (~$6M–$7M ARR, $35M raised) | Cloud-managed telemetry, system health, and infrastructure dashboard platform connecting distributed homelab servers and containers. |
| **[Elestio](https://elest.io)** | $11/month (billed hourly based on smallest VM size) | 3-day free trial with $20 credit (limited to deploying and testing up to 2 active services) | ~$550K ARR (Bootstrapped, no external institutional valuation) | Fully-managed DevOps hosting platform that deploys open-source homelab software onto dedicated cloud VMs with automated backups, SSL, and full root access. |
| **[PikaPods](https://www.pikapods.com)** | ~$1.80/month (metered hourly based on minimum CPU/RAM/storage pod allocation) | $5 welcome credit on signup (no credit card required, sufficient to run minimal pods for ~2-3 months); no permanent free-for-life tier | ~$200K–$500K Est. ARR (Bootstrapped via Peakford Ltd, no external institutional valuation) | Specialized managed 1-click container hosting service tailored for lightweight open-source homelab applications, bookmark tools, and utilities. |



## Open-Source GitHub Projects



- **[Heimdall](https://github.com/linuxserver/Heimdall)**  

  **The beginner-friendly default.** Drag-and-drop web UI, hundreds of pre-styled service tiles, and optional status checks that grey out dead links before they vanish . The PHP/Laravel stack is heavier than Go-based competitors but runs fine on a Raspberry Pi 4 . **Trade-offs**: limited widget support, restricted theming, and iconography some find dated . Best for first-time self-hosters who want a dashboard running in 10 minutes without touching a YAML file.



- **[Homarr](https://github.com/homarr-labs/homarr)**  

  **The Plex/*arr stack specialist.** Built specifically around media automation—Sonarr queues, Radarr calendars, SABnzbd progress, Plex sessions, and Pi-hole stats, all configured through a polished visual editor . **v1.x** added a modular widget system, multi-user authentication (OIDC/LDAP), and 89+ built-in integrations . **Trade-offs**: higher resource usage than minimalist alternatives, and backup/restore between instances is fiddly . Best for homelab admins whose dashboard doubles as a media server control panel.



- **[Dashy](https://github.com/lissy93/dashy)**  

  **The customization maximalist.** Themes, layouts, animations, widgets, sub-pages, status checks, search engines, and authentication—all configurable via YAML or a built-in UI editor . Ships with dozens of themes. **Trade-offs**: overwhelming for simple use cases, client-side Vue rendering is slower than server-side alternatives, and project pace has slowed in 2026 . Best for power users who want the dashboard to be a personal canvas and don't mind investing setup time.



- **[Flame](https://github.com/pawelmalak/flame)**  

  **The minimalist start page.** A search bar, clock, small weather widget, and a grid of links—that's it . Built-in GUI editors for apps and bookmarks, 11 search providers, authentication, custom CSS, and Docker label auto-discovery . Runs in a tiny Docker container with SQLite . **Trade-offs**: intentionally tiny widget library, no service status checks, and maintenance has slowed . Best for users who want a fast, search-first new tab page and nothing more.



- **[Homer](https://github.com/bastienwirtz/homer)**  

  **The simplest possible option.** A static page driven by a single YAML file with no backend . Footprint so small it runs on a Pi Zero. Configuration is trivial to back up (one file) and rendering is instant because there's no server-side logic . **Trade-offs**: links only—no widgets, no status checks, no dynamic data. Best for users who treat the dashboard as a static bookmark page and value simplicity above all.



### Additional Strong Open-Source Options



- **Homepage** — Best overall for live data. 100+ native service integrations with live widgets (download queues, media counts, system stats). YAML-configured, server-side rendered for fast loads . Best for anyone running 5+ services who wants a dashboard that shows real data, not just links.

- **Glance** — Lightweight dashboard for feeds and services. Best for users who want a modern, fast alternative to Flame with slightly more capability.

- **Organizr** — Tabbed interface for organizing HTPC and homelab services. Best for media-server-centric setups that want a unified tab experience .

- **Stackyard** — A calm, badge-focused dashboard with zero dependencies and no charts. Widgets are small visuals that only appear when something's wrong. Apache 2.0 licensed . Best for users who want a quiet dashboard that doesn't demand attention.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- **There are no SaaS products in this category**—homelab dashboards are fundamentally self-hosted tools. Hosted deployment convenience (Railway, PikaPods) wraps the same open-source software.

- **Dashboard choice depends on what you value**: Heimdall for ease, Homarr for *arr integrations, Dashy for customization, Flame for minimalism, Homepage for live data. No single option wins across all criteria .

- Self-hosted dashboards require proper authentication configuration if exposed beyond your LAN. Most options support password protection; review each project's security guidance.



---



**Made for homelab enthusiasts, self-hosters, and anyone who wants a private, fast start page for their services.**  

Let's make homelab dashboards more open, understandable, and appropriately minimal.
