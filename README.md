# Michael Wootan

Operator turned builder. I spent the last several years running a multi-channel e-commerce business (DTC and B2B wholesale) and building the automations that kept it running: order and fulfillment tracking, AI-assisted customer support, catalog onboarding, email marketing, content, SEO operations, and monitoring. Before that: logistics, supply chain, and project management.

I'm moving into **solutions engineering and implementation** roles, where the job is the same one I've been doing for my own business: understand how an operation actually works, then connect the systems so it runs with less manual work.

All of the projects below ran in production for a live e-commerce business in 2026, most of them on a schedule through GitHub Actions. Store names, customer data, and product details have been replaced with placeholders.

## Operations and customer experience

| Project | What it does | Stack |
|---|---|---|
| [ai-support-agent](https://github.com/Michael-Wootan/ai-support-agent) | Chat widget and email-triage pipeline on Claude: identity-verified order lookup, tiered escalation, 16-category email classification, dry-run mode and a replay eval harness | Python, Cloudflare Workers, Claude API, Shopify, IMAP/SMTP |
| [order-fulfillment-sync](https://github.com/Michael-Wootan/order-fulfillment-sync) | Shopify orders and carrier tracking into a shared ops sheet, with business-day SLA logic, an order state machine, exception alerts and a daily supplier email | Python, Shopify GraphQL, Google Sheets, USPS tracking |
| [shopify-product-listing-pipeline](https://github.com/Michael-Wootan/shopify-product-listing-pipeline) | Git-driven catalog onboarding: a product spec committed to a folder becomes draft Shopify products with images, FAQs and collections, plus a summary email and a feedback loop | Node.js, Shopify Admin API, Gemini, GitHub Actions |
| [automation-health-monitor](https://github.com/Michael-Wootan/automation-health-monitor) | Daily report on every scheduled automation: reads GitHub Actions runs and logs and emails what ran, what failed, and what it did | Node.js, GitHub API, SMTP |

## Marketing and growth

| Project | What it does | Stack |
|---|---|---|
| [ai-email-campaign-engine](https://github.com/Michael-Wootan/ai-email-campaign-engine) | Weekly campaigns built from store data, drafted in MailerLite, approved or held by email reply, with open and click stats fed back into the next run | Node.js, Claude API, MailerLite, Shopify, IMAP |
| [shopify-ai-content-pipeline](https://github.com/Michael-Wootan/shopify-ai-content-pipeline) | Keyword queue to published blog post: Claude drafting, originality and cannibalization guardrails, image generation, Shopify publishing and indexing | Node.js, Claude API, Google Sheets, Shopify, Copyscape |
| [ecommerce-contact-sync](https://github.com/Michael-Wootan/ecommerce-contact-sync) | Consent-filtered sync of Shopify customers into MailerLite groups, with an approval email before anything uploads | Node.js, Shopify, MailerLite, IMAP |
| [weekly-exec-report](https://github.com/Michael-Wootan/weekly-exec-report) | Weekly executive brief: SEO and revenue data pulled from APIs, analyzed by Claude, delivered as an HTML email | Node.js, Ahrefs API, Shopify, Claude API |
| [brand-mention-monitor](https://github.com/Michael-Wootan/brand-mention-monitor) | Scheduled scan of Reddit via the official API, summarized by Claude and emailed as a digest | Python, Reddit API, Claude API, GitHub Actions |

## Shopify and SEO tooling

| Project | What it does | Stack |
|---|---|---|
| [search-console-indexing](https://github.com/Michael-Wootan/search-console-indexing) | Automates Google Search Console indexing requests, status checks and not-indexed diagnosis within API quotas | Node.js, Google Search Console / Indexing API |
| [shopify-seo-redirects](https://github.com/Michael-Wootan/shopify-seo-redirects) | Bulk URL redirects and noindex controls through the Shopify Admin API | Node.js, Shopify Admin API |
| [shopify-theme-injectors](https://github.com/Michael-Wootan/shopify-theme-injectors) | Theme changes applied through the Asset API with timestamped backups and one-command revert | Node.js, Shopify Theme API, Liquid |

## What I work with

**Platforms:** Shopify, MailerLite, HubSpot, Google Workspace, Cloudflare, GitHub Actions, Apollo, Clay 
**Integration:** REST and GraphQL APIs, webhooks, OAuth, scheduled jobs, LLM APIs (Claude, OpenAI, Gemini)
**Languages:** Python, JavaScript / Node.js
**Operations:** fulfillment and carrier workflows, SLA tracking, catalog management, customer support operations, B2B wholesale

## Contact

[LinkedIn](https://www.linkedin.com/in/mwootan/) · [Email](mailto:michael.wootan66@gmail.com)
