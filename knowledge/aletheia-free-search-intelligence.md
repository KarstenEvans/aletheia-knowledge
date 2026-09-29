---
title: Aletheia Free Search Intelligence — Google, Bing and affiliate-research methods
slug: aletheia-free-search-intelligence
status: source-checked-knowledge-and-proposed-workflow
knowledge_type: original research and development guidance
last_checked: 2026-09-29
public_html: none
related_task: AK-098
source_class: Revenue Tactics promotional descriptions plus independently checked first-party provider documentation
---

# Aletheia Free Search Intelligence: what people search for, without paid-tool dependency

> **Aletheia Markdown | Knowledge-only.** This is original, independently sourced research, not a copy of the Revenue Tactics paid course, a completed course, a deployed Aletheia app, or verified access to private Google/Bing account data.
>
> [Aletheia Protocol](https://github.com/KarstenEvans/aletheia-protocol) governs source receipts, claim status, uncertainty, corrections and approval. [Thalia Protocol](https://github.com/KarstenEvans/thalia-protocol/blob/main/THALIA_PROTOCOL.md) permits optional appropriate humour without displacing evidence.
>
> Decisions: **FREE FIRST; no subscriptions, paid spying tools, ad spend, required card/billing setup, invented metrics, unauthorised scraping, auto-posting or auto-purchasing.** Study Revenue Tactics as an example of marketing architecture, not as an independent recommendation of the courses or software it advertises. Research input: [course catalogue](https://www.revenuetactics.com/our-courses/), [affiliate-linked tools page](https://www.revenuetactics.com/tools-resources/), reviewed 2026-09-29. The catalogue offers brief descriptions; their actual paid lessons were not accessed. The tools page explicitly discloses affiliate links.

## The question: can we see the most common Google and Bing searches?

Partly, but distinguish **general trending topics** from **estimated keyword search volume**, **searches that exposed our own verified site**, and **AI citation activity**. There is no single free, complete, exact public database of every query on Google and Bing. Report the engine, geography, language, time interval, sampled/estimated/actual-own-property status, last-checked date and tool restrictions with each metric. Do not add figures from different engines or treat a normalised score as an absolute count.

| Question | Free-first source | What it really tells us | Boundary |
|---|---|---|---|
| What is rising in Google searches in a place? | [Google Trends Explore](https://trends.google.com/trends/explore) | Normalised, sampled search *interest* (0–100); compare topic/term, region and time. | **100 is not a number of searches.** Low-volume zero is not proof of zero searches. |
| What is unusually popular right now in Google? | [Google Trends Trending Now](https://trends.google.com/trending?geo=GB) | Time-sensitive trending clusters, with displayed volume bands. | Trending/rising is not an exhaustive all-time or highest-volume chart. |
| What is sought over longer time periods? | Trends Explore; optional [Trends public BigQuery datasets](https://support.google.com/trends/answer/12764470) | Comparisons; documented BigQuery top/rising datasets for specified regions. | BigQuery is not the default free-first path; account, usage, eligibility and costs must be checked before enabling. |
| Estimated monthly Google searches for a term? | [Google Ads Keyword Planner](https://support.google.com/google-ads/answer/7337243/use-keyword-planner) | Estimated monthly searches, ideas and advertiser forecasts. | Free tool, **but Google says completed Ads setup including billing information is needed** to access basic features; skip under strict no-billing policy. Estimate, not a census. |
| Which Google searches expose our own pages? | [Google Search Console Performance](https://support.google.com/webmasters/answer/7576553) | Verified-property query/page/country/device clicks, impressions, CTR, average position. | Not all searches, only our property. Queries may be withheld/aggregated; API does not guarantee all rows. |
| Which Bing keywords/questions are popular? | [Bing Webmaster Keyword Research](https://www.bing.com/webmasters/help/keyword-research-628070b6) | Bing keyword volumes/trends, related/question terms, geography/language/device and recent terms; available time ranges within previous six months per current help. | Bing source, not a claim about Google. Newly discovered terms are *not necessarily newly searched*. |
| Which Bing searches expose our own pages? | [Bing Webmaster Search Performance](https://www.bing.com/webmasters/help/refreshed-webmaster-tools-7c7d2533) | Verified-property clicks/impressions by page/keyword. | Not the whole search universe. |
| How often is our content cited in supported AI answers? | [Bing Webmaster AI Performance](https://www.bing.com/webmasters/help/ai-performance-9f8e7d6c) | Aggregated citation activity, cited pages, grounding-query groups and time trends from supported Microsoft experiences. | Grounding groups are **not literal user prompts**, citations do not equal clicks, and numbers are sampled/limited; preview fields may change. |
| Estimated Microsoft search advertising demand? | [Microsoft Advertising Keyword Planner](https://www.about.ads.microsoft.com/en/tools/planning/keyword-planner) | Free to use *with a Microsoft Advertising account*: search-volume trends and ad estimates. | Do not initiate campaign, paid account obligation or advertising without explicit approval. |

**Primary sources:** [Trends sampling/normalisation FAQ](https://support.google.com/trends/answer/4365533?hl=en-GB), [Search Console metrics](https://support.google.com/webmasters/answer/7042828), [Search Console API limitations](https://developers.google.com/webmaster-tools/v1/searchanalytics/query), [Bing Webmaster free signup](https://www.bing.com/webmasters/help/getting-started-checklist-66a806de).

## Other free official tools and how to use them

- [Google Search Console](https://search.google.com/search-console/) for indexing/canonical/robots/sitemap problems and page-specific discovery. Verify each permitted site; never pretend a property has been connected when it has not.
- [Bing Webmaster Tools](https://www.bing.com/webmasters/) for search performance, keyword research, backlinks, Site Scan and AI Performance. May import a verified Google Search Console property subject to explicit user authorisation. [Bing Webmaster REST API](https://learn.microsoft.com/en-us/bingwebmaster/) can eventually support owner-authorised collection, but legacy SOAP/POX APIs were scheduled for retirement on 2026-08-31; use documented REST methods only.
- [Google PageSpeed Insights](https://pagespeed.web.dev/) and [Google Rich Results Test](https://search.google.com/test/rich-results) as optional public-URL technical checks; eligibility in a test does **not** guarantee a rich result.
- [Microsoft Clarity](https://clarity.microsoft.com/pricing) states that its heatmaps/session-recording feature set is free. It is **optional**, not preinstalled: complete the privacy, cookie/storage, consent, redaction, retention and accessibility assessment before adding user-behaviour recording; see [ICO storage/access guidance](https://ico.org.uk/for-organisations/direct-marketing-and-privacy-and-electronic-communications/guide-to-pecr/cookies-and-similar-technologies/).
- Autocomplete and related searches can offer *ideas*; neither Google nor Bing autocomplete suggestions alone establish an actual search count or ranking. Store any observed suggestions as date/place/device-specific exploratory leads, not verified volume.
- A free manual CSV export or account-owner-authorised API is preferred to unauthorised scraping or undisclosed, unstable Trends endpoints. Never publish personal search-console query exports containing private account data by default.

## Source inspiration vs. what we reuse

Revenue Tactics markets the Native Ads Master Class (public syllabus) and brief descriptions of organic SEO, email, YouTube/social and PPC courses. Its tools page includes ActiveCampaign (email), Voluum (tracking), AdPlexity/Anstrex (competitive ads), Convertri (landing pages), MaxBounty/ClickBank (affiliate networks), Taboola/Revcontent/MGID (paid ads). These are **promotional/vendor claims and affiliate links**. The paid course content, merits, conversion claims and student outcomes have not been independently evaluated. Extract the general pipeline only:

**Understand a real audience question → identify a real source → make useful original content → clear mobile landing page → check discovery and actual usage → test an improvement → record results and correct mistakes.**

No copy of proprietary syllabus/lessons, fabricated case study, advertorial disguise, fake scarcity, automatic paid advertising or bulk AI filler. Organic traffic and relevant answers come before commissions. Comparison claims and income claims need independently checkable context; a vendor paying commissions to reviewers is a material connection to disclose.

### ClickBank: research-only affiliate-marketplace lead

[ClickBank Marketplace](https://www.clickbank.com/) is a potential source of product/offer *leads*, not evidence of product efficacy or an Aletheia recommendation. ClickBank states account signup is free, but [its fee page, updated August 2026](https://support.clickbank.com/en/articles/10535137-what-are-clickbank-s-fees) lists a **$49.95 one-time activation fee when a seller's first product is approved**, a **$5 payment-period processing fee**, plus transaction pricing. Distinguish seller fees from affiliate participation and verify the precise current terms before any account action. Do not open an account as part of this note. Do not infer a high commission means a trustworthy product. Review merchant identity, actual offer, renewal/subscription disclosures, health/financial claims, refund conditions, UK audience suitability, first-party substantiation, consumer reviews, conflicts, advertising standards and live landing page. Continue existing Awin/Bookshop options only when contextually relevant and disclosed. No paid ClickBank-related software.

## Aletheia design and implementation contract (proposed, not deployed)

**One reusable Search Intelligence panel** for Aletheia Improve/Publisher/Discover/Trust Check. Default place = visitor's location **only after permission**; otherwise town/country entry and optional nearby suggestions. Allow worldwide location and language selection. Never silently force Swindon/London; keep source geography and time zone.

Input: subject or page URL, location, language, time window, source selection (Google Trends; Bing Keyword Research; account-owner Google/Bing performance CSV), and optional compare terms. Output must say source, `metric_type` (normalised_interest | approximate_volume | own_property_impression | own_property_click | ai_citation | exploratory_suggestion), `unit`, `engine`, `location`, `language`, `date_range`, `captured_at`, `access_method`, `evidence_url`, `coverage_limit`, and `verified_or_idea`.

Default screens: **WHAT PEOPLE ASK** (real questions) / **TRENDING** (labelled interest) / **OUR PAGES** (owner-uploaded first-party metrics) / **IMPROVEMENT IDEAS**. Show a compact answer-first card, timeframe/region and visual badge such as RISING, ESTIMATED or OUR SITE ONLY. Offer deeper method and source behind MORE. Never imply live access without connected account/actual fetch and never convert a published source link to an affiliate target.

### Cross-project improvements
- **Improve:** compare genuine FAQ/query gaps to visible source content; inspect clicks, impressions, CTR, technical quality, dates and indexing before changing metadata. Baseline/after in comparable geography/window; do not claim causal uplift from a simple before/after.
- **Discover / Mystika:** location-first demand signals only as editorial prompts; confirm actual local events, dates and places with primary/event-owner sources; one worldwide service, no mass-generated city clone pages. A rising search is not a verified event.
- **Publisher:** use a genuine audience need, source receipt, original expertise, duplicate check and human approval gate. Avoid a keyword-driven content farm, invented earnings or automatic social posting. Allow `NO_POST`.
- **Trust Check:** source/affiliate connection disclosure; separate independently checked product evidence from marketplace ranking and vendor sales assertions. Label recurrent marketing tropes as leads to verify rather than imputing dishonest motives. Compare advertised vs verifiable terms and date checked.

### Free-first acceptance checks
1. Source + period + geography are visible and accurate; 100/relative interest is never presented as a search count.
2. Bing keyword counts, Google Trends bands, own-site impressions/clicks and AI citations never share an unqualified metric column or get summed.
3. If external data cannot be accessed, show a labelled manual-import/open-source link and no simulated live data.
4. Account details, bills, paid trials, ad launches, recordings, affiliate signups and publishing require **separate human approval**; for now avoid billing-required paths.
5. Sensitive/regulated products (especially medical, financial and miraculous-income offers) are never recommended from conversion/commission statistics alone.
6. Source links remain ordinary links; optional disclosed affiliate recommendations are separate, genuinely relevant and not in source citations.
7. Human checks one pilot using a UK topic and an outside-UK comparison, desktop/mobile, without requiring paid software.


## Updated public tool shelf and film-affiliate research (2026-09-29)

The companion standalone public HTML is maintained in the separate Apps repository: [Affiliate Tools](https://karstenevans.github.io/aletheia-app/aletheia-site-audit/affiliate-tools.htm) and its [rebuild specification](https://github.com/KarstenEvans/aletheia-app/blob/main/aletheia-site-audit/aletheia-site-audit-page.md). The HTML has `Books / Gifts` as the final burger-menu option, with free reading **ahead of** optional shopping. It includes [Accessibility for Everyone](https://accessibilityforeveryone.site/) by Laura Kalbag: genuinely freely readable on the author's successor/publisher site; originally published 2017, openly shared since 2025, with the author's explicit warning that some cited tools may be outdated. No paid affiliate link is needed to access it.

Additional independently sourced no-cost/optional tools, not inherited from the Revenue Tactics sales list:

| Tool | Official source and reason | Boundary |
| --- | --- | --- |
| WAVE single-page checker and local browser extension | [WAVE](https://wave.webaim.org/) / [extension](https://wave.webaim.org/extension/). Human accessibility review assisted by checks for errors/structure. | Free checker/extension; optional API paid. Automated test is not proof of WCAG compliance. |
| WebAIM colour contrast | [Contrast Checker](https://webaim.org/resources/contrastchecker/). Test text/background colour ratios. | Individual pair, not complete page approval. |
| W3C Nu HTML checker | [Modern HTML validator](https://validator.w3.org/nu/) and [W3C tools](https://www.w3.org/QA/Tools/). | Validation does not guarantee usability or ranking. |
| Bing IndexNow | [Official get-started](https://www.bing.com/indexnow/getstarted). Owner can submit changed/added/deleted site URLs to participating search engines. | Requires an ownership key. Acknowledgement does not guarantee indexing, and it is not ordinary Google indexing submission. |
| Google Data Studio | [Current product docs](https://docs.cloud.google.com/data-studio/welcome). The former Looker Studio was renamed **Data Studio in April 2026**. No-cost data reporting tool. | Requires account, optional individual data connectors may have distinct fees, Pro is paid. |
| Google Alerts | [Official help](https://support.google.com/websearch/answer/4815696?hl=en). Opt-in emails for matching newer search results. | Not a full archive or exact keyword search volume. |

**Film research:** Disney confirms [Hocus Pocus (1993)](https://movies.disney.com/hocus-pocus) and a [UK Disney+ film page](https://www.disneyplus.com/en-gb/browse/entity-b99c38fd-44ae-402f-b727-bc7fccb63740), but **no specific current Aletheia-approved Disney+ affiliate referral** has been established. [Rarewaves has a specific UK Region-2 Hocus Pocus DVD page](https://www.rarewaves.com/products/5017188882095-hocus-pocus-region-b2), barcode **5017188882095**. Awin publicly lists [Rarewaves merchant profile ID 70042](https://ui.awin.com/merchant-profile/70042) and [World of Books UK ID 116709](https://ui.awin.com/merchant-profile/116709). These merchant listings are **research leads only**, not proof Aletheia's publisher account is approved, any item is in stock, any personal tracking URL exists, or a film-streaming programme is available. All public gift-page links remain ordinary `data-awinignore` links pending separate authorised approval. ClickBank's [Marketplace guide](https://support.clickbank.com/en/articles/10535269-what-is-the-clickbank-marketplace) explains its seller-offer model, but no legitimate/rights-cleared Disney/Hocus Pocus film offering was independently verified there. Never promote an unclear seller's movie/stream as a legitimate studio release merely because it is on a marketplace.

The historic name **“Trust Partner”** remains unresolved, not silently identified as TradeTracker, Tradedoubler, Partnerize or a current business. Preserve it as a research question rather than fabricating a match.

The [Aletheia Constellation](https://github.com/KarstenEvans/aletheia-app/blob/main/shared/README.md) adds **curated editorial crosslinks** to standalone Aletheia HTML, with one dated link/icon JSON catalogue. The Halloween `🧙` link to [Halloween Gifts & Resources](https://karstenevans.github.io/aletheia-app/seasonal/halloween-gifts.htm) appears between 1 September and 10 November inclusive; ordinary stars return 11–24 November, and winter sprites run 25 November–31 December. No seasonal sprite links to an unbuilt gift page. This is navigation, not an affiliate-advertising layer. No course-making, auto-posting, paid ad expenditure or false earning claims are introduced by this update.

## Sources and provenance (checked 2026-09-29)

- [Revenue Tactics public course index](https://www.revenuetactics.com/our-courses/) — seller's course descriptions, not independently verified outcomes.
- [Revenue Tactics tools page](https://www.revenuetactics.com/tools-resources/) — seller-curated list with disclosed affiliate links.
- [Google Trends FAQ](https://support.google.com/trends/answer/4365533?hl=en-GB); [Trending Now](https://trends.google.com/trending?geo=GB); [BigQuery dataset](https://support.google.com/trends/answer/12764470).
- [Google Ads Keyword Planner help](https://support.google.com/google-ads/answer/7337243/use-keyword-planner); [Google Search Console performance](https://support.google.com/webmasters/answer/7576553); [API query limits](https://developers.google.com/webmaster-tools/v1/searchanalytics/query).
- [Bing Webmaster Keyword Research](https://www.bing.com/webmasters/help/keyword-research-628070b6); [Search Performance](https://www.bing.com/webmasters/help/refreshed-webmaster-tools-7c7d2533); [AI Performance](https://www.bing.com/webmasters/help/ai-performance-9f8e7d6c).
- [Microsoft Advertising Keyword Planner](https://www.about.ads.microsoft.com/en/tools/planning/keyword-planner); [Microsoft Clarity pricing](https://clarity.microsoft.com/pricing); [ICO guidance](https://ico.org.uk/for-organisations/direct-marketing-and-privacy-and-electronic-communications/guide-to-pecr/cookies-and-similar-technologies/); [ClickBank fees](https://support.clickbank.com/en/articles/10535137-what-are-clickbank-s-fees).

**Status:** Knowledge and reusable design specification only. No account connected, paid tool purchased, privacy tracker installed, data collected, new app built, public HTML page added, automatic posting enabled or advertiser campaign launched.