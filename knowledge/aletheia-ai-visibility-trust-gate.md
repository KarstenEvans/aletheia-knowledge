---
title: "The Invisible Website: Aletheia AI Visibility and Trust Gate"
slug: aletheia-ai-visibility-trust-gate
status: source-checked-original-research; deployment and site-specific crawler testing pending
knowledge_type: original source-traced practical guide
reviewed: 2026-10-20
source_scope: Contentsquare/AWS guide introduction and public summary; official Google and OpenAI crawler guidance
public_html: companion proposed in KarstenEvans/aletheia
---

# The Invisible Website: Aletheia AI Visibility and Trust Gate

[Aletheia Protocol](https://github.com/KarstenEvans/aletheia-protocol) governs evidence, uncertainty, challenges and correction. [Thalia Protocol](https://github.com/KarstenEvans/thalia-protocol) supports optional presentation without replacing evidence. [Aletheia Trust Check](https://github.com/KarstenEvans/aletheia-app/blob/main/aletheia-trust-check/aletheia-trust-check.md) examines identity, claims and reputation. [Aletheia Site Audit](https://github.com/KarstenEvans/aletheia-app/blob/main/aletheia-site-audit/aletheia-site-audit.md) measures technical reachability and discoverability.

> **First, an Aletheia Trust Check. Then an Aletheia Site Audit. Then optimisation.** This is a workflow recommendation, not proof that a site is good or bad. A failed fetch, missing recommendation or indexing problem MUST NOT automatically become a negative trust verdict.

## The gated-community problem

A site may be excellent for human visitors but invisible to search or AI retrieval systems. Causes include DNS/TLS failures, unintentional robots.txt exclusions, server or CDN firewall challenges, rate limits, authentication walls, robots meta noindex rules, empty JavaScript-only HTML, broken internal links, unavailable sitemaps or poor discoverability. HTTPS is ordinarily *helpful*, not a reason to hide a site. Do not accuse a particular host, including Fasthosts, of blocking AI without reproducible target-specific evidence.

The stages are separate:
1. **Identity and safety**: confirm the exact domain, ownership claims, impersonation clues, security warnings and material factual claims, with source citations and correction paths.
2. **Reachability**: check HTTPS and HTTP, apex/www redirects, certificate, real status codes, bot-vs-browser access, CDN/WAF challenges and DNS.
3. **Crawl permissions**: fetch the *actual* /robots.txt for every host, inspect named user-agent groups, sitemaps, noindex directives and server responses.
4. **Index/discovery eligibility**: check that meaningful public HTML, canonicals, titles, descriptions, internal links and sitemap URLs are accessible. Google Search Console and Bing Webmaster Tools give owner-verified evidence when connected.
5. **Answerability and attribution**: provide accurate original material, clear who/what/where/when facts, primary references, author or publisher context, visible corrections and stable public URLs.
6. **Recommendation/selection**: test a dated set of relevant questions across multiple engines, recording whether a source was directly cited, linked, absent or misdescribed. Nonappearance is NOT proof of distrust.

## Different crawlers have different jobs

The official [OpenAI crawler overview](https://developers.openai.com/api/docs/bots) differentiates:
- **OAI-SearchBot**: search discovery for ChatGPT Search; owners can allow or disallow it independently.
- **GPTBot**: model-training crawler; refusing training does not, by itself, mean refusing ChatGPT Search.
- **ChatGPT-User**: may fetch a page in response to a user's request; not automatic search-crawling control. Robots rules may not always apply to these user-initiated visits.

Do not recommend indiscriminately allowing every bot. Legitimate crawler identity should be verified against published IP guidance or appropriate verification, not trusted merely because the User-Agent claims a name. Keep authentication/private areas protected. A site can choose to allow search discovery while declining foundation-model training.

Google says pages need to be indexed and snippet-eligible to appear as supporting links in Google's AI search features. Technical eligibility does **not** guarantee indexing, ranking, citation or recommendation. See [Google guidance for generative AI Search](https://developers.google.com/search/docs/fundamentals/ai-optimization-guide) and [AI features](https://developers.google.com/search/docs/appearance/ai-features).

An optional **llms.txt** is a supplementary description/discovery aid, NOT an established universal AI-indexing requirement or substitute for crawlable HTML, a sitemap or robots.txt.

## Evidence states and diagnosis

For each host/URL and named crawler, record: timestamp UTC; tested hostname/path; user-agent and verified IP if available; request method; HTTP status; redirect chain; response title and meaningful HTML excerpt; robots rule; noindex; DNS/TLS; authentication/challenge evidence; checked tool; result; and confidence.

Use **OBSERVED**, **SOURCE DOCUMENTED**, **INFERENCE**, **NOT TESTED**, and **UNKNOWN**. Do not represent a web-tool refusal as evidence that the origin server refused the same request.

| Observation | What it may mean | What it does not prove | Next step |
| --- | --- | --- | --- |
| Human browser loads; named bot gets 403/429 | WAF/host/bot policy, rate limiting or network difference | Host is fraudulent or AI placed it on a reputation blacklist | Compare origin/CDN logs and verified bot request |
| /robots.txt disallows OAI-SearchBot | Site-owner search-crawl restriction | GPTBot training is automatically blocked too | Confirm intentional policy and assess effect |
| Site reachable but not indexed | New pages, duplicate/canonical, noindex, crawlability or ranking | An AI has judged the business dishonest | Use Search Console URL Inspection and site evidence |
| HTTP 200 but no meaningful HTML | Client rendering or thin/empty content | Broken HTTPS | Add clear server-rendered or static human-readable content |
| One AI omits a site | Retrieval, query, relevance, freshness or index differences | Universal AI blacklist | Repeat neutral prompts across systems and dates |
| HTTPS/TLS errors | Certificate, redirect, host configuration or legacy cache | Fasthosts blocks all AI | Reproduce per host and affected client |

## Ethical optimisation, after the Trust Gate

- Make a genuinely useful public page for each real visitor question; avoid keyword stuffing, manufactured FAQs and mass-produced near-duplicates.
- Put the answer in normal HTML text, supported by accessible mobile navigation, source links and dated evidence.
- Publish canonical URLs, descriptive titles, sensible metadata, legitimate structured data when content warrants it, and a sitemap reflecting real public pages.
- Maintain identity and contact/correction routes. Clearly disclose affiliations, sponsored links and experimental tools.
- Track owner-verified Search Console and Bing measures separately from AI referral analytics. Referral data is incomplete: AI answers may contain no link or may be copied into other applications.
- Use a small repeatable query panel. Count mentions, citations, factual accuracy, user usefulness and genuine conversion, not just raw impressions.
- Fix actual safety weaknesses; do not weaken authentication/firewalls merely to get bots in.

## Project-specific starting points (20 October 2026)

**Swindon.org.uk:** public homepage and topic pages were retrieved in an external web search on 20 October 2026, so the site is not globally invisible. This observation does NOT demonstrate access for OAI-SearchBot, GPTBot, Googlebot or every URL. Production robots/sitemap/TLS/host logs remain **NOT VERIFIED** here. Keep local Swindon facts on the local portal. Owner should verify in Search Console and inspect origin access logs before asserting a Fasthosts-wide cause.

**Aletheia, the Worldwide AI site:** the [canonical GitHub repository](https://github.com/KarstenEvans/aletheia) describes a separate GitHub Pages discovery hub, connecting [Apps](https://github.com/KarstenEvans/aletheia-app), [Knowledge](https://github.com/KarstenEvans/aletheia-knowledge), [Protocol](https://github.com/KarstenEvans/aletheia-protocol), Learn and original articles. Publication/source does not prove every public URL has been indexed. Maintain distinct publisher metadata and useful HTML for the hub.

**Aletheia Learn:** the AI Fluency course already teaches RAG, hallucination, source checking and risk, but lacked a dedicated practical website-visibility laboratory when reviewed on 20 October 2026. Add a small *optional* exercise, without changing the 0-9 lesson sequence.

**Trust Check:** distinguish (a) technical unreachable, (b) absent from AI answers, (c) documented site safety warning and (d) evidence-based business credibility. Require a correction/dispute pathway; never automatically suppress a domain merely for failure to appear in an answer.

## What we took from Contentsquare and AWS

Source inspiration: [Contentsquare's *AI traffic acquisition guide* public summary](https://go.contentsquare.com/en/marketing-cro-ai), a commercial marketing publication with AWS contributors. The user-provided saved webpage exposes the guide's introduction and expert list but not a reliably extractable complete 15-page PDF. Accordingly **the exact remaining numbered tips have NOT been independently verified**. Its reported growth percentages and 2030 forecasts are claims, not Aletheia results or universal predictions. We adapt the public themes (AI as an acquisition channel, AI-readable content, reduced user friction, measurement and iteration) and add the missing independent Trust Gate, crawler-policy distinction, correction rights and privacy-by-design.

This is an **original commentary and technical field guide**, not a reproduction of the source publication.

## Reusable 30-day experiment

- **Days 1-7:** Trust Check; obtain real DNS/TLS/robots/sitemap and bot log receipts; establish two canonical public hosts and an indexation baseline.
- **Days 8-14:** repair only observed discovery blockers; preserve server security and privacy; submit real sitemap URLs if appropriate.
- **Days 15-21:** publish or improve three genuinely useful answer pages (one Swindon local page, Aletheia hub overview, one AI Learn lesson) with cited primary sources.
- **Days 22-30:** rerun the same prompts and technical checks. Record actual changes and limitations; do not claim higher AI rankings without repeated evidence.

### Sources (reviewed 20 October 2026)

1. Contentsquare/AWS, *The AI traffic acquisition guide*, public summary: https://go.contentsquare.com/en/marketing-cro-ai
2. OpenAI, official crawler roles: https://developers.openai.com/api/docs/bots
3. Google, generative AI search optimisation: https://developers.google.com/search/docs/fundamentals/ai-optimization-guide
4. Google, AI features indexing rules: https://developers.google.com/search/docs/appearance/ai-features
5. Google, robots.txt basics: https://developers.google.com/search/docs/crawling-indexing/robots/intro

**Status:** Research and proposal. Live bot access, true logs, indexing and conversion measures require owner tools and independent verification.