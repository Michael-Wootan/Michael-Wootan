# Michael Wootan

Operator turned builder. I spent the last several years running a multi-channel e-commerce business (DTC and B2B wholesale) and building the systems that ran its revenue and operations: outbound prospecting, reply handling, lead routing, market intelligence, AI customer support, order tracking, lifecycle email, content and monitoring. Before that: B2B sales, logistics and supply chain.

I'm looking at **GTM engineering and solutions engineering** roles, where the job is the one I've been doing for my own business: understand how a revenue team or an operation actually works, then connect the systems so it runs with less manual work.

Every project below ran in production for a live business in 2026, most of them on a schedule through GitHub Actions. Company names, customer data and product details have been replaced with placeholders.

**Areas:** [GTM and outbound](#gtm-and-outbound-systems) · [Lifecycle email](#lifecycle-email) · [Partner and PR outreach](#partner-and-pr-outreach) · [Market intelligence](#market-and-competitor-intelligence) · [Operations](#operations-and-customer-experience) · [Reliability](#monitoring-and-reliability) · [SEO and content](#seo-and-content-tooling)

## GTM and outbound systems

| Project | What it does | Stack |
|---|---|---|
| [outbound-engine](https://github.com/Michael-Wootan/outbound-engine) | Daily cold outbound: Apollo people search across rotating segments, credit-capped email reveal, Claude-personalized copy, staggered sends, contacted and bounce dedupe, dry-run mode and a 21-day domain warmup ramp | Node.js, Apollo API, Claude API, SMTP, GitHub Actions |
| [ai-reply-triage](https://github.com/Michael-Wootan/ai-reply-triage) | Reads the outreach inbox, suppresses bounces, skips auto-replies and classifies real replies into five intents with Claude (with a prompt-injection guard). A clear yes gets the promised asset sent automatically; everything else is forwarded with a suggested reply | Node.js, IMAP/SMTP, Claude API |
| [followup-sequencer](https://github.com/Michael-Wootan/followup-sequencer) | Follow-up cadence over the outreach logs: day 4 bump, day 10 breakup, reply detection by sender or subject, stale contacts marked cold without a send, suppression list and per-run send caps | Node.js, IMAP/SMTP |
| [interested-lead-sync](https://github.com/Michael-Wootan/interested-lead-sync) | Moves cold-email leads labeled Interested or Meeting booked into the right nurture group by campaign. Idempotent upserts, auto-detection of new campaigns and a summary email | Node.js, Instantly API, MailerLite API |
| [outreach-funnel-dashboard](https://github.com/Michael-Wootan/outreach-funnel-dashboard) | Weekly rollup across every outreach channel: sends, replies, reply rate, follow-up activity and how many days of targets are left in the pool | Node.js, SMTP |

## Lifecycle email

| Project | What it does | Stack |
|---|---|---|
| [ai-email-campaign-engine](https://github.com/Michael-Wootan/ai-email-campaign-engine) | Weekly campaigns built from store data, drafted in MailerLite, approved or held by email reply, with open and click stats fed back into the next run | Node.js, Claude API, MailerLite, Shopify, IMAP |
| [ecommerce-contact-sync](https://github.com/Michael-Wootan/ecommerce-contact-sync) | Consent-filtered sync of Shopify customers into MailerLite groups, with an approval email before anything uploads | Node.js, Shopify, MailerLite, IMAP |

## Partner and PR outreach

| Project | What it does | Stack |
|---|---|---|
| [partner-prospecting](https://github.com/Michael-Wootan/partner-prospecting) | Builds a pool of sites from Ahrefs competitor link data, finds and validates a contact email on each, sends a personalized pitch and runs its own follow-up cycle with a 90-day cooldown | Node.js, Ahrefs API, Claude API, SMTP |
| [competitor-link-prospecting](https://github.com/Michael-Wootan/competitor-link-prospecting) | Weekly discovery of sites that link to competitors, pitches drafted into a queue and sent in weekday batches. Discovery and sending run as separate modes to protect API quota | Node.js, Ahrefs API, Claude API, GitHub Actions |

## Market and competitor intelligence

| Project | What it does | Stack |
|---|---|---|
| [market-demand-radar](https://github.com/Michael-Wootan/market-demand-radar) | Demand scan across 8 countries: product-intent keywords scored by volume and difficulty, year-over-year growth and momentum from volume history, all inside a hard API credit budget | Node.js, Ahrefs API |
| [weekly-exec-report](https://github.com/Michael-Wootan/weekly-exec-report) | Weekly executive brief: SEO and revenue data pulled from APIs, analyzed by Claude, delivered as an HTML email | Node.js, Ahrefs API, Shopify, Claude API |
| [brand-mention-monitor](https://github.com/Michael-Wootan/brand-mention-monitor) | Scheduled scan of Reddit via the official API, summarized by Claude and emailed as a digest | Python, Reddit API, Claude API, GitHub Actions |

## Operations and customer experience

| Project | What it does | Stack |
|---|---|---|
| [ai-support-agent](https://github.com/Michael-Wootan/ai-support-agent) | Chat widget and email-triage pipeline on Claude: identity-verified order lookup, tiered escalation, 16-category email classification, dry-run mode and a replay eval harness | Python, Cloudflare Workers, Claude API, Shopify, IMAP/SMTP |
| [order-fulfillment-sync](https://github.com/Michael-Wootan/order-fulfillment-sync) | Shopify orders and carrier tracking into a shared ops sheet, with business-day SLA logic, an order state machine, exception alerts and a daily supplier email | Python, Shopify GraphQL, Google Sheets, USPS tracking |
| [shopify-product-listing-pipeline](https://github.com/Michael-Wootan/shopify-product-listing-pipeline) | Git-driven catalog onboarding: a product spec committed to a folder becomes draft Shopify products with images, FAQs and collections, plus a summary email and a feedback loop | Node.js, Shopify Admin API, Gemini, GitHub Actions |

## Monitoring and reliability

| Project | What it does | Stack |
|---|---|---|
| [automation-health-monitor](https://github.com/Michael-Wootan/automation-health-monitor) | Daily report on every scheduled automation: reads GitHub Actions runs and logs and emails what ran, what failed, and what it did | Node.js, GitHub API, SMTP |

## SEO and content tooling

| Project | What it does | Stack |
|---|---|---|
| [shopify-ai-content-pipeline](https://github.com/Michael-Wootan/shopify-ai-content-pipeline) | Keyword queue to published blog post: Claude drafting, originality and cannibalization guardrails, image generation, Shopify publishing and indexing | Node.js, Claude API, Google Sheets, Shopify, Copyscape |
| [search-console-indexing](https://github.com/Michael-Wootan/search-console-indexing) | Automates Google Search Console indexing requests, status checks and not-indexed diagnosis within API quotas | Node.js, Google Search Console / Indexing API |
| [shopify-seo-redirects](https://github.com/Michael-Wootan/shopify-seo-redirects) | Bulk URL redirects and noindex controls through the Shopify Admin API | Node.js, Shopify Admin API |
| [shopify-theme-injectors](https://github.com/Michael-Wootan/shopify-theme-injectors) | Theme changes applied through the Asset API with timestamped backups and one-command revert | Node.js, Shopify Theme API, Liquid |

## What I work with

**GTM stack:** Apollo, Instantly, HubSpot, Clay, MailerLite
**Platforms:** Shopify, Google Workspace, Cloudflare, GitHub Actions, Ahrefs
**Integration:** REST and GraphQL APIs, webhooks, OAuth, IMAP/SMTP, scheduled jobs, LLM APIs (Claude, OpenAI, Gemini)
**Languages:** Python, JavaScript / Node.js
**Operations:** outbound and reply handling, lead routing, fulfillment and carrier workflows, SLA tracking, customer support operations, B2B wholesale

## Contact

[LinkedIn](https://www.linkedin.com/in/mwootan/) · [Email](mailto:michael.wootan66@gmail.com)
