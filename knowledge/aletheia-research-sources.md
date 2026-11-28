---
title: Aletheia Research Sources
version: 0.1.0
status: shared-research-module
updated: 2026-11-28
---

# Aletheia Research Sources

[Aletheia Protocol](https://github.com/KarstenEvans/aletheia-protocol) | [Thalia Protocol](https://github.com/KarstenEvans/thalia-protocol/blob/main/THALIA_PROTOCOL.md)

## Purpose

A shared, provider-independent register of scholarly discovery sources for Aletheia Knowledge, Trust Check, AI-PI, Go Walkabout, research prompts and relevant Aletheia apps. Use original research and authoritative records wherever available. The register is not a local copy of these repositories, an installed connector, or proof that any search has run.

## Core sources

| ID | Source | Coverage / role | Search | Programmatic access |
|---|---|---|---|---|
| ARXIV | arXiv | Computing, AI, maths, physics, quantitative biology; preprints and some subsequently published works | https://arxiv.org/ | https://info.arxiv.org/help/api/user-manual.html |
| PUBMED | PubMed | Biomedical and clinical literature citations and abstracts; links to available full text | https://pubmed.ncbi.nlm.nih.gov/ | https://www.ncbi.nlm.nih.gov/books/NBK25501/ |
| EUROPEPMC | Europe PMC | Life sciences, abstracts, available full text, preprints and citation links | https://europepmc.org/ | https://europepmc.org/RestfulWebService |
| BIORXIV | bioRxiv | Biological and molecular science preprints | https://www.biorxiv.org/ | https://api.biorxiv.org/ |
| MEDRXIV | medRxiv | Medical and health science preprints | https://www.medrxiv.org/ | https://api.biorxiv.org/ |

The bioRxiv/medRxiv API supports date and DOI lookups and publication links; use the web search or Europe PMC for topical discovery where appropriate. Not every interface supports arbitrary keyword searching. API documentation links checked; live API requests not tested. Direct access to bioRxiv/medRxiv information pages was blocked during this review; their shared API documentation was accessible.

## Supporting sources

| ID | Source | Role | Search / access |
|---|---|---|---|
| PMC | PubMed Central | Free full-text biomedical literature; reuse rights vary | https://pmc.ncbi.nlm.nih.gov/ |
| OPENALEX | OpenAlex | Scholarly discovery across disciplines; citation graph | https://openalex.org/ ; https://help.openalex.org/api/ |
| CROSSREF | Crossref | DOI, metadata, publication versions, corrections and retraction metadata where available | https://search.crossref.org/ ; https://www.crossref.org/documentation/retrieve-metadata/rest-api/ |
| CTGOV | ClinicalTrials.gov | Trial registration, design and reported results; registry entries are not proof of efficacy | https://clinicaltrials.gov/ |
| COCHRANE | Cochrane Library | Healthcare systematic reviews; some full text may be restricted | https://www.cochranelibrary.com/ |

For healthcare recommendations also consult relevant authoritative guidance (e.g. NICE, NHS, WHO and applicable professional guidelines); for technical research consult primary specifications, official documentation and source code. No requirement to search irrelevant sources merely to complete a checklist.

## Default research procedure

1. Define the question, relevant disciplines, terms, synonyms and dates. Check existing Aletheia knowledge nodes first where available.
2. For scientific DEEP research, check all five core sources for relevance. Search each materially relevant source, directly or through a transparent indexed route such as Europe PMC; explicitly name sources covered indirectly. For QUICK research use the smallest adequate subset.
3. For health, prioritise PubMed and Europe PMC, then bioRxiv and medRxiv for emerging work, arXiv where relevant to the topic. For AI/technical research prioritise arXiv, OpenAlex and original code/specifications; add biomedical sources for interdisciplinary research.
4. Look for systematic reviews, replicated human studies, original experiments, and evidence that contradicts the proposed hypothesis. Separate human, animal, in-vitro, computational and theoretical findings.
5. Retrieve original records and full text when legally available. Mark FULL_TEXT, ABSTRACT_ONLY, METADATA_ONLY or NOT_ACCESSED. Do not assert a result was read if only metadata was retrieved.
6. Deduplicate by DOI, PMID, PMCID, arXiv ID, title/author and linked preprint/journal versions. Preserve relationships; do not treat multiple versions as independent replication. Check publication, correction, withdrawal and retraction status. Preprints are preliminary, not equivalent to peer-reviewed clinical evidence.
7. Record source, search terms, date, coverage and limitations: DIRECT_SEARCHED, INDEXED_ROUTE_SEARCHED, NOT_RELEVANT, UNAVAILABLE or NOT_SEARCHED. Distinguish no relevant hits from not searched. Do not claim exhaustive coverage.
8. Extract only useful atomic knowledge nodes, retaining original provenance and uncertainty. Do not silently convert a hypothesis, association or mechanism into a causal clinical claim. Retain contradictory evidence and unresolved possibilities.
9. Use free-first access and respect API limits, licences and privacy. If an API or search is unavailable, report it and use an available route; never fabricate results. Do not upload private medical information or personal identifiers to research services without authorisation.
10. STOP when sufficient evidence has been obtained for the decision. Go Walkabout is an optional bounded exploration, not automatic recursion.

## Suggested portable knowledge record

```yaml
node_id: <stable-project-id>
statement: <one precise finding or claim>
statement_type: <Aletheia Protocol type>
source_title: <original paper title>
source_url: <direct original record>
identifiers:
  doi: null
  pmid: null
  pmcid: null
  arxiv_id: null
publication_status: <preprint / peer-reviewed / other / unknown>
evidence_design: <human RCT / observational / animal / in-vitro / computational / other>
access_status: <FULL_TEXT / ABSTRACT_ONLY / METADATA_ONLY / NOT_ACCESSED>
population_or_model: <where relevant>
limitations: <material caveats>
related_nodes: []
contradictory_evidence: []
checked_on: <YYYY-MM-DD>
```

This is an illustrative extraction template, not a replacement for the normative protocol schema. Use canonical protocol fields, revision and provenance requirements for any claimed conformance.

## Short prompt for reuse

> Apply Aletheia Research Sources. For scientific DEEP research, assess all five core sources (arXiv, PubMed, Europe PMC, bioRxiv and medRxiv), search the relevant ones and report direct, indirect, unavailable and irrelevant coverage. Use PubMed Central, OpenAlex, Crossref, ClinicalTrials.gov and Cochrane as appropriate. Retrieve original evidence, distinguish preprints and published versions, deduplicate studies, look for contradictions, label evidence type and access limitations, and extract portable Aletheia knowledge nodes with DOI/PMID/source links and uncertainty. Never claim searches or verification not performed. Use free-first access; STOP when sufficient.

## Integration

Canonical GitHub location: `KarstenEvans/aletheia-knowledge/knowledge/aletheia-research-sources.md`. Link this one register from relevant bootloaders, research workflows, Trust Check HEALTH/DEEP, AI-PI and scientific knowledge prompts rather than duplicating the list. Retain domain-specific source lists where they already exist. Load it on demand when a scientific or scholarly task requires it; no background monitoring, automatic imports or paid APIs are enabled by this module. If a host cannot load it, disclose the limitation and use relevant accessible official sources without claiming the register was loaded.
