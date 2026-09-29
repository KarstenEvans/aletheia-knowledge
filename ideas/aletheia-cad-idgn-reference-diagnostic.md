# Aletheia CAD Assistant — iDGN Reference Diagnostic

> **Aletheia Markdown | Approved project idea and developer handover**  
> Created: 29 September 2026 | Status: IDEA / priority research and prototype, NOT yet built or tested  
> Project task: **AK-093**. This is a **priority development task**, not Priority #001, which remains Worldwide Aletheia Discover.  
> Proposed component: **Aletheia iDGN Reference Diagnostic** (within Aletheia CAD Assistant).  
> Protocols: [Aletheia Protocol](https://github.com/KarstenEvans/aletheia-protocol) (source receipts, uncertainty, contradictions and approval); [Thalia Protocol](https://github.com/KarstenEvans/thalia-protocol/blob/main/THALIA_PROTOCOL.md) (optional humour, never in error reports).  
> Origin: Karsten's MicroStation/iDGN working experience and proposed exchange-based diagnostic, inspired at a broader automation level by [James Lord's AI/CAD LinkedIn post](https://lnkd.in/p/etMW-rZS). The external post is NOT evidence of this diagnostic's feasibility.

## 1. Executive concept

**Find the few troublesome published iDGN references in a large model without manually opening 50 files or trying to compress read-only published content.**

A master MicroStation design file may have dozens of attached reference files or models. On direct opening of an affected file, MicroStation may emit the warning **“Large Level Name dictionaries were encountered”** and accompanying detail in Message Center. The operator's current **Compress Design, Include References** workflow does not conveniently provide a durable list associating each direct-open warning with the exact source filename. There may be only two or three suspect items in a 50-reference arrangement.

Build an inventory, then test each eligible reference as the *active file* using a verified **Reference Exchange / XD= or direct-open route**, capture startup warnings and timings, and produce an actionable path-by-path report. **The first version is diagnostic and strictly non-destructive; it must not compress or modify iDGN or live engineering design content.**

### What this is NOT
- Not an unattended “fix my CAD” button; not a replacement for the originating model owner, design review or controlled republishing.
- Not an assertion that every slow model is caused by the level-name dictionary.
- Not proof that saved views, dynamic sections, render information or any single category causes this precise message; investigate these as possible *other forms of accumulated file data*, and keep their evidence separate.
- Not a generic Python file parser that pretends it can reliably inspect Bentley's full DGN/iDGN semantics without supported SDK access.
- Not a claim that an embedded reference in a packaged i-model is a separately openable file.

## 2. Problem and evidence classification

**Observed user workflow (operational input):**
1. Load an active DGN/iDGN aggregation model; its reference tree can contain around 50 references.
2. A generic large-level-name-dictionary warning appears in connection with open/loading; operators use **Compress Design with Include References**, or the key-in \`COMPRESS DESIGN INCLUDEREFS\`, to inspect/improve eligible *writable* files.
3. The available workflow does not give the operator the file-by-file attribution they need, particularly in a read-only published iDGN/ProjectWise environment.
4. The message becomes apparent when the suspect reference is opened *as the active file*, not necessarily when seen only as an attached reference.
5. Manually identifying and exchanging/opening every source, recording messages and returning to the master is repetitive.

**Verified product background, with caveats:**
- Bentley describes a published i-model as **read-only** and its typical filename as \`.i.dgn\`; \`.dgn.i.dgn\` can denote the published master originating from a DGN. References may be separately published or embedded when the **Package** option is used. See Bentley's [i-model FAQ](https://bentleysystems.service-now.com/community?id=kb_article_view&sysparm_article=KB0040931) and [publishing overview](https://bentleysystems.service-now.com/community?id=kb_article_view&sysparm_article=KB0111013).
- Bentley documents a **Reference Exchange** workflow that opens an attached reference as the active document. A historical official macro is an example, not a compatible or endorsed implementation for every current release: [Exchange references with this macro](https://bentleysystems.service-now.com/community?id=kb_article_view&sysparm_article=KB0055338).
- A [historical key-in reference](https://www.codot.gov/content/business/designsupport/CADDmanual/Documentation/MicroStationKeyinReference.pdf) lists \`XD=\` for exchanging the active file with a reference. **Parameter syntax, file permissions, embedded-content and current-version behaviour require testing.**
- A CAD technical article discusses the precise warning, level-name dictionary accumulation and \`COMPRESS DESIGN INCLUDEREFS\`: [MicroVisie 2015/1](https://tmc-nederland.nl/protected_download.php?file=%2Fwp-content%2Fuploads%2F2018%2F03%2FMicroVisie-2015-1.pdf). This is historical guidance, not proof of behaviour or thresholds in the installation under test.

**Unverified implementation hypotheses:** the warning can be captured programmatically with correct file association at the direct-open/exchange boundary; direct opening a separate read-only iDGN will reproduce the operator's message; embedded packaged references may need a distinct test route. Validate before claiming a working solution.

## 3. Primary user story

> As a BIM/CAD information coordinator, I can run a read-only scan from the active MicroStation master, enumerate its real referenced files and models, open/exchange into the eligible targets one by one, capture the warnings shown on activation, and export a unique list of suspect filenames, so I can direct any authorised remediation or republishing at the correct source.

### Desired operator flow

1. Open master model normally in MicroStation; start **ALETHEIA → iDGN REFERENCE CHECK**.
2. Display current master name, active model, MicroStation version/build, workspace/workset and whether files are managed by ProjectWise.
3. Discover active and optionally nested references; show a preview of **unique physical file + model candidates**, including file path, attachment logical name, nesting parent, format, load/display status, resolved/missing path, permissions and embedded/packaged status if exposed.
4. Choose diagnostic depth: **direct references** (MVP) or **nested / transitive references** (later). Deduplicate by canonical file identity while retaining all attachment paths as provenance. Avoid cycles.
5. Confirm **SCAN READ-ONLY**. The tool snapshots starting file/model and current state, and enables its own logging **before** each direct open or exchange.
6. For each eligible candidate, either use a version-tested **Exchange / XD=** operation or a supported direct-read-only-open API. **Do not confuse switching between models inside one container with opening a physical referenced file.** Capture identity from the active design file *after* switching, to prevent associating a message with the wrong candidate.
7. Record Message Center startup message text, severity, timestamps, open outcome, elapsed time and any structured count/details returned by supported API. Close/return safely, then continue. If the event API proves unavailable, test a supported output/logging route before considering any UI capture.
8. Export human-readable **HTML/Markdown plus CSV/JSON**. Default to local file output, no upload or telemetry.
9. Show one-click copy/export of **suspect filenames** plus a full evidence table; preserve *not scanned*, *permission denied*, *embedded*, *missing*, *timed out*, and *no warning observed* as different states.
10. Offer a separately gated future **remediation assessment**, never automatic in version 1.

## 4. Reference enumeration specification

For every attachment collect, subject to exposed SDK data:

| Field | Meaning |
|---|---|
| scan_id, parent_id, attachment_id | Stable per-scan trace through reference nesting |
| master_file, parent_file, parent_model | Original model and intermediate attachment origin |
| logical_name, attachment_name, attachment_model | As attached/displayed, not a substitute for physical identity |
| reported_path, resolved_path | Preserve original and resolved form; do not guess absent values |
| ProjectWise identifier, datasource (if available) | Managed-document identity without exposing credentials |
| type, read_only, embedded, missing, loaded | Capability/status facts, with UNKNOWN when not exposed |
| canonical_file_key and model key | Deduplication target; retain every referencing parent |
| depth, cycle_detected | Recursive safety |
| scan_strategy | direct-open, exchange, model-only diagnostic or unsupported |

**Critical distinction:** 50 attachment rows may represent fewer than 50 physical files. A packaged i-model may contain embedded models with no ordinary standalone pathname. Deduplicate physical file opens but retain each model/attachment relationship. If the warning is model-dependent, support per-model inspection after per-file testing.

No implicit write access, checkout/check-in or extraction from protected packages. Respect ProjectWise permissions and workset configuration; an unresolved path is a reportable result, not an automatic “bad file”.

## 5. Diagnostic algorithm (pseudocode, NOT an installed key-in script)

\`\`\`text
snapshot original master, active model, application/workspace and permissions
start scan receipt and persistent diagnostic log
inventory attached references and model relationships
resolve supported file identities; classify embedded/ordinary/missing
deduplicate physical files; retain all parent attachment paths
for each eligible physical file:
    checkpoint pending candidate, intended route and start time
    clear or mark message capture boundary
    direct-open READ-ONLY or Exchange via tested MicroStation route
    verify actual active file/model identity; if mismatch report MISMATCH
    capture startup Message Center messages and relevant structured status
    record elapsed time, warnings, exact text, severity and source identity
    persist result immediately so a later crash does not lose earlier records
    return/reopen original master safely, or isolate each test in a controlled run
for unsupported embedded targets:
    report EMBEDDED / NEEDS PACKAGE-SPECIFIC METHOD, not CLEAN
restore original state where supported; never write the design files
generate CSV, JSON and human-readable report
\`\`\`

**Potential complication:** changing the active DGN may unload a VBA/MDL session or reset a message listener. The prototype must test whether the controller survives Exchange/OpenDesignFile; if not, use a startup-loaded MicroStation add-in, durable external queue + checkpoint file, or separate per-candidate launch under a controlled application session. Never attribute a stale warning to the next file.

**Warning matching:** store verbatim text and use a case-insensitive matching rule for \`large level name dictionar*\` as a flag only. Persist all warnings to allow review of other startup issues. Use the actual MicroStation version and raw message, not an invented dictionary-count metric.

## 6. Suggested output

File: \`aletheia-idgn-scan-YYYYMMDD-HHMM.csv\`; accompanying readable \`.md\`/\`.html\` and machine-readable \`.json\`.

| File (example only) | Parent / attachment | Direct-open status | Warning | Time | Result |
|---|---|---|---|---:|---|
| \`A-PUBLISHED-01.i.dgn\` | \`MASTER.dgn → STRUCTURE\` | Opened read-only | Large Level Name dictionaries… | 7.4 s | REVIEW |
| \`B-PUBLISHED-02.i.dgn\` | \`MASTER.dgn → CIVIL\` | Opened read-only | None observed | 2.1 s | NO TARGET WARNING OBSERVED |
| \`PACKAGE.i.dgn::embedded-model-3\` | \`MASTER.dgn → PACKAGE\` | Separate file unavailable | Not tested | n/a | EMBEDDED / INCONCLUSIVE |
| \`C-PUBLISHED-03.i.dgn\` | \`MASTER.dgn → MEP\` | Access denied | Not tested | n/a | ACCESS DENIED |

These are **illustrative invented filenames and timings**, not real results. A missing warning is **not** a guarantee the file is healthy. Report counts separately for candidate attachments, unique files, tested files, suspected files, unsupported embedded targets, and failures.

CSV minimum schema: \`scan_id,candidate_id,master_file,parent_file,attachment_name,attachment_model,resolved_file,active_file_confirmed,is_embedded,is_read_only,strategy,open_status,warning_matched,warning_text,severity,start_time_utc,elapsed_ms,notes\`. Escape CSV safely; JSON retains exact message newlines.

Human-facing result: filter **Suspects / All / Not Tested**, copy filenames, show raw Message Center receipts, highlight repeated paths and include an optional sorted time report. Never display an invented root-cause verdict or default to destructive cleanup.

## 7. Implementation alternatives

### A. MicroStation VBA prototype (first feasibility probe)
Use familiar VBA object model, iterate active file's reference attachments, try documented application methods for file opening, and test whether Message Center information can be captured in the running build. Good for a small feasibility probe, but long sessions, controller survival across document change and exact startup-message capture need evidence.

### B. MicroStation SDK MDL C++ / .NET add-in (probable production approach)
Prefer supported application-side APIs for attachments, active-file transitions, event/message capture and UI. Acquire **the SDK matching the deployed MicroStation version**, compiler and runtime. Do not assume a 2023 CONNECT SDK matches a later MicroStation product build. [Bentley SDK releases](https://bentleysystems.service-now.com/community?id=kb_article_view&sysparm_article=KB0012597); [Bentley programming starting point](https://bentleysystems.service-now.com/community?id=kb_article_view&sysparm_article=KB0012628). Evaluate available SDK event hooks and logging APIs with actual installed headers/samples; no unverified function names here.

### C. Python orchestration (optional, not a standalone DGN reader)
Python can prepare scan queues, launch a supported MicroStation batch/add-in or COM automation path if available, parse returned logs and generate HTML/CSV. Do not assume Python by itself can directly parse proprietary attachments, invoke an in-process message listener or bypass managed-document permissions. Retain MicroStation as the authoritative test environment.

### D. Standard Batch Process / key-in as fallback
Probe whether Batch Process can open each unique filename in a controlled context, call a non-mutating logger and retain a one-file-one-message receipt. **Do not use \`COMPRESS DESIGN INCLUDEREFS\` as a diagnostic batch on protected live iDGN.** The exact \`XD=\` syntax and selection behaviour must be recorded from an actual experiment; a static guessed key-in is not an acceptable implementation.

**Decision gate:** choose the smallest method that can reproduce the exact warning, identify the actual active physical document, persist logs across file transitions, and leave all inputs unchanged.

## 8. Safety, access and engineering information management

- **Read-only default**. Do not invoke Compress, VerifyDGN Repair, Save Settings, reference detach, edits, update libraries, republish, or ProjectWise checkout during diagnosis.
- Prefer local/offline operation. Never send client/rail project drawings, paths, metadata, screenshots or logs to public AI or an external service without employer authorisation. Sanitise any sample shared for development.
- Snapshot original state and preserve a locally stored resumption checkpoint. On crashes, report last completed candidate; do not silently resume with a destructive key-in.
- Handle nested/duplicate references and circular attachments; limit depth, batch size and timeouts.
- Differentiate warning provenance: detected on master opening, detected on candidate direct open, detected in unrelated DGNLIB/workspace, missing reference, or permission issue.
- For ProjectWise, use authorised document resolution and avoid assuming ordinary Windows path semantics; do not bypass locks, ACLs or managed file handling.
- A remediation stage, if approved separately, may identify responsible *source editable DGN(s)*, owner, publishing pipeline and safe backup/republish route. It must present preview/dry-run and human approval. Published iDGN remains immutable.

## 9. Acceptance tests

1. In an authorised, anonymised dataset with 1 master and 5 distinct external reference files, implant/identify a known positive warning in one candidate. Scanner lists the exact filename and verbatim startup warning, not just a total count.
2. Where 2 attachments point to the same physical file, scan once and retain both parent/attachment links.
3. Include a clean candidate and verify status is **no target warning observed**, not “perfectly clean.”
4. Include a missing file and permission-denied file: neither is misreported as negative.
5. Include an embedded packaged reference: classify correctly and do not invent a separate file to Exchange.
6. Verify returned active file path/model matches the queued target before accepting warning attribution.
7. Simulate a crash halfway; earlier results and pending queue remain recoverable.
8. Confirm master and every test file's file hash/modified timestamp (where lawful and feasible) unchanged after read-only scan. Account for harmless ProjectWise local cache side effects separately.
9. Test in same MicroStation version/build, workspace/workset, ProjectWise status and configuration as actual operations.
10. Export correct CSV/JSON/Markdown with counts, elapsed time, exact messages, dates, evidence and limitations.

**MVP success definition:** the tool demonstrably finds the 2 or 3 named problem *files* amongst a representative many-reference model with no source modifications. Quantitative time savings need measured baseline and prototype results, not projection.

## 10. Information and materials needed for the first prototype

- MicroStation product, edition and exact version/build, architecture, Windows version; whether OpenBuildings/AECOsim and ProjectWise integration are in scope.
- An authorised **sanitised sample master + 3–5 referenced sample files**, including one known-warning case; or a reproducible non-confidential sample built locally. Prefer a small separately published \`.i.dgn\`, plus an embedded/packaged case if possible.
- Screenshot or *verbatim* Message Center startup text, with sensitive paths redacted; optional Message Center detail/Compress summary.
- Screenshot of the Reference dialog/tree and actual packaging/embedded tooltip, with filenames redacted.
- Whether \`XD=\` can exchange to a read-only published file in the installed build; test manually and capture what happens when a reference is embedded.
- MicroStation SDK access/licence, API documentation, actual samples and matching VS toolchain.
- Permission to inspect only local/project-approved material. **No confidential HS2 or third-party engineering data to a public repository.**

## 11. Development phases and next actions (AK-093)

- [ ] Confirm exact startup warning with a sample and distinguish it from other large-reference symptoms.
- [ ] Inventory separate vs embedded published i-models and nested DGN/iDGN reference layouts.
- [ ] Manually demonstrate **Exchange / XD=** into one eligible read-only reference; record actual supported syntax and active-file identity. Check return-to-master workflow.
- [ ] Determine reliable event/message capture: SDK listener, message details export or a supported logger. Begin capture before transition.
- [ ] Prototype 3–5 targets; persist one row per file and parent attachment references; verify originals unchanged.
- [ ] Choose VBA vs C++/.NET MDL vs MicroStation-driven Python orchestration based on confirmed API behaviour.
- [ ] Produce CSV and readable HTML/Markdown reports with warnings, source trail and unsupported states.
- [ ] Test 50-reference case including duplicates, nested files, ProjectWise/unresolved paths and one packaged i-model.
- [ ] Add the tested code, build instructions, required SDK, known limitations, sample *synthetic* data and adjacent public page specification only after review.
- [ ] Keep future “identify writable source and recommend controlled republish/compress” as a separately approved stage.

## 12. Handover to the next AI/developer

Read current repository guides (\`README.md\`, \`aletheia-knowledge-GUI.md\`, \`aletheia-knowledge-code.md\`, \`aletheia-knowledge-tasks.md\`) and this file before edits. Confirm actual installed Bentley environment and source access. **First deliverable is a reversible, read-only *proof of warning attribution***; do not spend time building a polished UI or claim file repair before a warning can reliably be captured against a verified active filename. Use evidence receipts and state what was tested, inferred, blocked and not tested. GitHub is the canonical text master; no real confidential client CAD files in it.

### Sources / reading trail (checked as background on 29 September 2026)

- [Bentley: i-model FAQ; read-only, separate vs packaged reference behaviour](https://bentleysystems.service-now.com/community?id=kb_article_view&sysparm_article=KB0040931)
- [Bentley: introduction to publishing i-models](https://bentleysystems.service-now.com/community?id=kb_article_view&sysparm_article=KB0111013)
- [Bentley: Exchange references with this macro (historical)](https://bentleysystems.service-now.com/community?id=kb_article_view&sysparm_article=KB0055338)
- [CDOT historical MicroStation key-in reference, XD=](https://www.codot.gov/content/business/designsupport/CADDmanual/Documentation/MicroStationKeyinReference.pdf)
- [Bentley: CONNECT SDK releases and prerequisites](https://bentleysystems.service-now.com/community?id=kb_article_view&sysparm_article=KB0012597)
- [Bentley: MicroStation programming resources](https://bentleysystems.service-now.com/community?id=kb_article_view&sysparm_article=KB0012628)
- [MicroVisie 2015/1: Level Name Dictionary warning and historical compress behaviour](https://tmc-nederland.nl/protected_download.php?file=%2Fwp-content%2Fuploads%2F2018%2F03%2FMicroVisie-2015-1.pdf)

**Provenance:** User's original proposed troubleshooting route and requirements are firsthand operational context; product behaviour above is separately attributed. No runnable tool has been created or safety-tested by writing this document.
