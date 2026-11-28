# Aletheia Ageing War: Inhibit the Inhibitors

Status: KNOWLEDGE-ONLY / RESEARCH PROJECT / NOT TREATMENT ADVICE  
Version: 0.3.0  
Created: 18 November 2026  
Last evidence review: 19 November 2026  
Scope: cellular senescence, inflammatory signalling, macrophage reprogramming, NAD metabolism, immune evasion, pancreatic cancer, and the risks of indiscriminate inhibition.  
Project principle: **Reveal harmful cells, restore useful clearance, redirect immune signals; inhibit only where necessary.**

> This public file records research hypotheses and independently attributable findings. It is neither a cancer-treatment protocol nor an instruction to use medicines, supplements or unapproved interventions. It contains no personal health information.

## Research continuation

For new investigations or material updates, retrieve [Aletheia Research Sources](https://raw.githubusercontent.com/KarstenEvans/aletheia-knowledge/main/knowledge/aletheia-research-sources.md) and apply its biomedical source and evidence rules. Distinguish human, animal, cell, computational and hypothesis-level findings; check linked preprint/publication versions and conflicting evidence. This workflow link does not update the last evidence-review date or establish a new treatment claim.

## Philosophy: the internal war is not simply good cells against bad cells

Many biological signals have two or more roles. A protective signal may be hijacked by diseased cells; a normal immune reaction may contribute to age-related metabolic dysfunction; a molecule that blocks immune attack in one context can stimulate it in another.

**Inhibit the inhibitors** is only one tactic. Also test ways to expose recognition signals, restore immunity, redirect protein processing or trafficking, and selectively mark harmful cells. The research sequence is:

1. Identify the initiating cell and trigger, and distinguish a proved cause from a plausible upstream trigger.
2. Trace the message, receptor, signalling pathway, responding cell and downstream effect.
3. Ask whether the effect is physiological protection, pathological exploitation, or both.
4. Identify a selective interruption point, including the cost of losing the normal protective function.
5. Demand cell-type-specific, disease-specific and ideally human evidence before promoting a candidate as a therapy.

**New strategic principle: immune recognition and immune metabolism are related but different fronts.** Macrophages can contribute to chronic tissue NAD+ loss through CD38 *and* may fail to engulf tumour cells when tumour CD47 engages macrophage SIRPα. Do not infer that the same macrophage population, intervention or signalling pathway underlies both without evidence.

---

## WAR-IMM-001 | CD38: senescent cells can indirectly accelerate NAD+ consumption

### Summary
In ageing-related experimental research, inflammatory secretions from senescent cells (the senescence-associated secretory phenotype, SASP) promote the accumulation or activation of CD38-expressing immune cells, including macrophages. CD38 is an NAD-consuming enzyme. This provides a causal model for part of age-associated tissue NAD+ depletion.

### Mechanism, supported in preclinical systems
Senescent cells -> SASP inflammatory cytokines -> macrophage recruitment/activation and CD38 expression -> increased CD38-dependent NADase activity -> contribution to tissue NAD+ decline.

### What needs correcting in our earlier shorthand
- It is too narrow to write that macrophages detect senescent-cell ROS and therefore express CD38. Reactive oxygen species (ROS) can participate in senescence and inflammation, but the cited studies specifically demonstrated effects of secreted inflammatory signals, including SASP factors. The role of ROS as the *specific direct signal* in this chain is not established by those data.
- CD38 is primarily an NAD-consuming enzyme in this comparison, **not** the same sort of surface anti-phagocytosis instruction as CD47.
- The presence of CD38 on macrophages does not mean that macrophages are always harmful; their actions depend on activation state, tissue and circumstance.

### Evidence
EVIDENCE: Strong mechanistic preclinical evidence; limited basis for direct human therapeutic conclusions.  
Sources:
- Covarrubias AJ et al. *Senescent cells promote tissue NAD+ decline during ageing via the activation of CD38+ macrophages*. Nature Metabolism (2020). https://doi.org/10.1038/s42255-020-00305-3
- Chini CCS et al. *CD38 ecto-enzyme in immune cells is induced during aging and regulates NAD+ and NMN levels*. Nature Metabolism (2020). https://doi.org/10.1038/s42255-020-00298-z

---

## WAR-IMM-002 | CD47: pancreatic cancer cells can strengthen a macrophage 'don't eat me' signal

### Summary
A study published online on **13 November 2026** in *Gastroenterology* reports that interleukin-18 (IL-18) promotes STAT1-dependent expression of **CD47 on pancreatic ductal adenocarcinoma (PDAC) cells**. CD47 engages an inhibitory receptor called SIRPα on macrophages, reducing their ability to engulf the tumour cells.

### Mechanism
PDAC cell / tumour IL-18 -> STAT1 signalling -> higher tumour-cell CD47 -> binding to macrophage SIRPα -> reduced macrophage phagocytosis -> improved tumour survival.

This is **not** a claim that IL-18 becomes CD47 or that CD47 is the same molecule as CD38. IL-18 is a cytokine, STAT1 is a signalling/transcription regulator, CD47 is a cell-surface protein and SIRPα is an inhibitory receptor on macrophages.

### What the paper did
- Used genetically engineered mouse models of spontaneous PDAC with IL-18 depletion.
- Used single-cell RNA sequencing and functional assays to examine macrophages, tumour cells and their interactions.
- Found reduced tumour progression and longer survival when IL-18 was depleted in the mouse models.
- Identified a STAT1 -> CD47 mechanism by which IL-18 impaired macrophage-mediated phagocytosis.
- Found greater proportions of macrophages with antigen-presenting/phagocytic features (including MHCII and CD11c) after IL-18 depletion.
- Found that treatment with a KRAS inhibitor increased IL-18 expression in PDAC cells. In the IL-18-depleted experimental context, KRAS inhibition was more effective and macrophage-mediated clearance improved.

### The interpretation for our project
The tumour appears to **exploit a normal protection mechanism**, rather than manufacture an entirely new immune system. CD47 is present on many normal cells, including red blood cells. The cancer can strengthen that protective signal on its own surface; the macrophage receives the inhibition through SIRPα.

This connects with the Ageing War at the level of **cell-to-cell signalling and macrophage function**, but the specific CD38 and CD47 pathways have different outcomes and must not be conflated.

### Important limits
- **Preclinical**: the reported combination is not an established treatment in humans.
- The study supports specific mechanisms in tested PDAC models; it does not establish that all pancreatic cancers, all IL-18 producers or all macrophages behave identically.
- A published mechanistic target is not the same as a safe drug candidate. The paper investigated genetic IL-18 depletion; it did not validate a generally safe, clinically approved IL-18-blocking treatment.
- CD47-SIRPα protects normal blood cells. Systemically blocking this pathway has produced clinical challenges such as anaemia, thrombocytopenia and limited efficacy, making selectivity critical.

### Evidence
EVIDENCE: Direct mechanistic mouse-model and functional evidence, plus human tumour association; human combination efficacy unproven.  
Primary source: Sun X et al., *Depletion of Endogenous IL-18 Suppresses Pancreatic Cancer Progression, Reprograms the Tumor Microenvironment, and Enhances KRAS Inhibitor Efficacy*. Gastroenterology, online 13 Nov 2026. DOI: https://doi.org/10.1053/j.gastro.2026.10.383 . PubMed: https://pubmed.ncbi.nlm.nih.gov/43025768/  
Institutional report: https://www.mdanderson.org/newsroom/scientists-identify-key-immune-driver-of-pancreatic-cancer.h00-159860079.html  
CD47 checkpoint clinical caveats:
- Nature Reviews Cancer (2026), *Targeting phagocytosis checkpoints for cancer immunotherapy*: https://doi.org/10.1038/s41568-025-00893-w
- Review on CD47 expression in healthy cells and blood toxicities: https://pmc.ncbi.nlm.nih.gov/articles/PMC12477725/

---

## WAR-IMM-003 | IL-18 has opposing effects: avoid a blanket 'IL-18 is bad' conclusion

### Summary
In the new PDAC models, reducing IL-18 helped expose cancer cells to macrophage clearance. Yet IL-18 can also stimulate natural killer (NK) cells and T cells and has been *enhanced*, not blocked, in several other experimental cancer immunotherapy strategies.

### Crucial 'inhibit the inhibitors' paradox
- **PDAC setting in Sun et al. 2026:** IL-18 -> STAT1 -> tumour CD47 -> macrophage evasion. Selectively reducing this mechanism may help.
- **Other tumour settings:** IL-18 can contribute to anti-tumour NK/T-cell responses. A natural soluble binding protein, IL-18BP, restrains its action. Some investigational immunotherapies try to block IL-18BP or use IL-18 resistant to its binding, allowing more IL-18 signalling.
- Consequently, the instruction "inhibit IL-18" may be beneficial in one model and harmful in another. The instruction "inhibit the IL-18 inhibitor" may also be beneficial in some models and harmful in others.

### What decides the direction?
Tumour type; source of IL-18; receptor-expressing responding cells; macrophage phenotype; immune composition; signalling competence; relative free versus IL-18BP-bound IL-18; dose, distribution and timing; and the treatment being combined.

### Evidence
EVIDENCE: Preclinical and mechanistic evidence across distinct tumour contexts; no universal rule.  
Sources:
- Sun et al., Gastroenterology (2026): https://doi.org/10.1053/j.gastro.2026.10.383
- Zhou et al. / IL-18BP review (2026), *IL18BP in cancer: a double-edged sword and emerging therapeutic opportunity*: https://pmc.ncbi.nlm.nih.gov/articles/PMC13684787/
- *IL-18BP is a secreted immune checkpoint and barrier to IL-18 immunotherapy*, Nature (2020): https://doi.org/10.1038/s41586-020-2422-6
- *Decoy-resistant IL-18 reshapes the tumor microenvironment... in renal cell carcinoma*, JCI Insight (2025): https://pmc.ncbi.nlm.nih.gov/articles/PMC11721305/

---

## WAR-IMM-004 | Comparative checkpoint and inhibitor map

| Pathway | Principal source/context | Target / receiver | Outcome relevant to project | What a selective strategy would need to preserve |
| --- | --- | --- | --- | --- |
| Senescent-cell SASP -> CD38 | Senescent cells affect inflammatory macrophages | CD38 NADase in immune cells | Tissue NAD+ consumption, metabolic ageing mechanism | Necessary inflammation resolution, pathogen defence, normal CD38 functions |
| PDAC IL-18 -> STAT1 -> CD47 | Pancreatic tumour cells in the 2026 models | CD47 on tumour, SIRPα on macrophages | Less tumour-cell phagocytosis | CD47 protection of healthy cells; useful IL-18 immune stimulation |
| IL-18BP -> IL-18 restraint | Soluble IL-18 binding protein, multiple tissues | Free IL-18 availability to immune cells | Can constrain useful anti-tumour immunity or damaging inflammation | Tissue-appropriate inflammation control and immune safety |

**Other original Ageing War targets to integrate later:** PARP, NAMPT, SARM1, NNMT, senescence clearance, LPS/inflammageing and NAD salvage. These should have their own independently sourced cards before they are used in comparisons. NAMPT, for example, contributes to NAD salvage and must not be automatically categorised as a harmful inhibitor. This update does not claim these separate branches have been reviewed here.

### Compact philosophy
**Do not simply remove the body's brakes. Find out who has hijacked them, which brake is being pressed, and who needs that brake to survive.**

---

## WAR-IMM-005 | PS is a lipid to expose, not a substitute protein for CD47

### Summary
CD47 is a cell-surface protein encoded by the CD47 gene. PS (phosphatidylserine, PtdSer) is a **phospholipid** usually kept on the inner plasma-membrane leaflet. Changing CD47 mRNA translation cannot turn CD47 into PS: they are chemically and biosynthetically different materials. The relevant PS intervention question is **outer-surface exposure**, not necessarily producing more total PS.

Flippases ATP11A/ATP11C normally return PS inside. Scramblases including XKR8 (apoptosis-linked) and TMEM16F (calcium-activated) can expose PS outside. PS exposure can invite macrophage engulfment but can also promote immunosuppressive cleanup via receptors including TAM/TIM-family pathways. It is not a universally beneficial 'eat-me' trigger in cancer.

### Direct pancreatic-cancer proof of principle
Zhao et al. (*Journal of Clinical Investigation*, 17 November 2025) found that disrupting pancreatic cancer-cell de novo pyrimidine synthesis (CAD deficiency, or DHODH targeting) promoted macrophage-dependent UMP depletion, PS exposure and macrophage phagocytosis in mouse pancreatic cancer models. **CD47 surface levels stayed unchanged.** Tumour burden fell in tested models. The authors could not fully separate PS-driven engulfment of viable cells from recognition of cells entering early apoptosis. It is preclinical, not a human treatment.

### Evidence
- Primary: https://doi.org/10.1172/JCI193370
- Flippase/scramblase biology: https://pmc.ncbi.nlm.nih.gov/articles/PMC10134735/
- Counterevidence: prolonged PS exposure can drive tumour immune evasion: https://doi.org/10.1038/s41420-025-02789-y
- PS immune checkpoint review: https://pubmed.ncbi.nlm.nih.gov/38573347/

EVIDENCE: tested mouse PDAC mechanism; PS immune effects are context-dependent.

---

## WAR-IMM-006 | Make CD47 incorrectly: change maturation or destination rather than replace it with CD48

### Summary
A nucleated cancer cell continuously makes new CD47, whereas a circulating **mature** red blood cell lacks protein-synthesis machinery. This suggests a relative production-stage vulnerability, **not inherent tumour selectivity**: normal tissues and developing blood cells also manufacture CD47.

### Three production-line concepts
1. **Incorrect finishing / QPCTL:** QPCTL modifies newly synthesized CD47 to create N-terminal pyroglutamate (pGlu) important for SIRPα recognition. Experimental QPCTL loss or interference can preserve total surface CD47 while reducing its functional binding to macrophage SIRPα. A 2026 B-ALL study directly compared wild-type protein with a mutated CD47 N-terminal amino acid, finding poorer SIRPα binding in the latter. Neither finding demonstrates a selective approved PDAC treatment.
2. **Wrong delivery address / CD47 mRNA 3'-UTRs:** In a 2015 *Nature* study, long versus short CD47 mRNA 3'-UTRs encoded the **same protein sequence** but directed it differently. Long 3'-UTR CD47 was delivered efficiently to the cell surface; short 3'-UTR CD47 was largely retained internally. HuR/SET/RAC1-mediated trafficking contributes. Tumour-specific control of this mechanism is a research hypothesis.
3. **Wrong translated protein / RNA or DNA changes:** Gene or RNA editing can, in principle, alter a protein sequence. No validated strategy safely and uniformly reprograms CD47 across pancreatic tumours to generate a harmless replacement. Tumour targeting, tumour heterogeneity, non-cancer-cell effects and normal CD47 function are major obstacles.

**CD48 is a real, biologically active and unrelated immune signalling glycoprotein**, not an inert CD47 variant. It participates in CD2 and CD244 (2B4) pathways; expression could be useful or harmful depending on cell context. Converting CD47 into CD48 is not a one-step alternative.

### Complications
- Already circulating mature red cells cannot produce or process new CD47, but **newly developing** erythrocytes, other immune cells and normal nucleated tissues do, so a systemic processing/trafficking intervention is not automatically safe.
- Removing functional CD47 alone may be insufficient to trigger engulfment without a positive macrophage-activating cue.
- Broad PS exposure can push macrophages into tolerance; aim for defined tumour-specific outcomes rather than PS quantity alone.

### Evidence and original source links
- CD47 QPCTL maturation: https://doi.org/10.1038/s41591-019-0356-z
- CD47 Q1A mutation and SIRPα binding (B-ALL rather than PDAC): https://ashpublications.org/bloodneoplasia/article/doi/10.1016/j.bneo.2026.100242/568193/
- CD47 long vs short 3'-UTRs and protein localization: https://doi.org/10.1038/nature14321
- CD48 physiology and human immunity: https://jci.org/articles/view/191340
- CD48 dual effects in cancer: https://pubmed.ncbi.nlm.nih.gov/42500566

EVIDENCE: protein maturation and trafficking mechanisms experimentally demonstrated, tumour-selective therapeutic exploitation hypothetical.

### Go Walkabout priorities
1. Compare tumour-versus-normal pancreas **total CD47, functional pGlu-CD47, QPCTL, long/short CD47 3'-UTRs and surface CD47**.
2. Test whether IL-18/STAT1-mediated CD47 increases change dependence on CD47 maturation or trafficking.
3. Compare macrophage phagocytosis with PS exposed but CD47 unchanged, and with defective CD47 but no extra PS cue.
4. Record erythrocyte precursors, normal tissues, immune-cell adverse effects, macrophage inflammatory polarization and human trial evidence.
5. Explore tumour-specific delivery and markers without assuming a single pan-cancer solution.

---

## WAR-IMM-010 | What prevents PS from reaching the outer membrane? ATP11A/C, CDC50A and the two-switch paradox

### Summary
Phosphatidylserine (PS/PtdSer) is a phospholipid normally kept mainly on the **cytoplasmic (inner) leaflet** of healthy plasma membranes. P4-ATPase **flippases ATP11A and ATP11C**, working with the chaperone **CDC50A** (encoded by **TMEM30A**), actively transfer exposed PS back inward using ATP. **Scramblases XKR8 and TMEM16F/ANO6** permit relatively rapid bidirectional transfer; XKR8 is caspase-activated in apoptosis, whereas TMEM16F responds to raised intracellular calcium in viable cells.

### Mechanistic answer to 'could we inhibit what inhibits PS exposure?'
Yes in principle: reducing inward flippase activity removes a brake on outer-surface PS exposure. **However, flippase inactivation alone is generally insufficient to cause *rapid* PS externalization**, because the charged PS headgroup crosses the hydrophobic membrane core extremely slowly without an active transport route. In normal apoptosis, caspases coordinate **ATP11A/C inactivation + XKR8 activation**. During some transient calcium elevations, calcium suppresses ATP11A/C function while activating TMEM16F. Increased PS synthesis is not necessarily required.

**This biology is essential in healthy cells** for coagulation (particularly platelets), immune-cell activation, efferocytosis, membrane polarity, signalling and red-cell stability. There is no justified general approach of globally inhibiting flippases or activating scramblases.

### Direct falsification test: more exposed PS made tumours grow *faster*
A 2022 *Cell Reports* primary study (Xue et al., 41:111582) disabled **Tmem30a/CDC50A** in MC38 mouse colon adenocarcinoma cells. The living cancer cells constitutively exposed surface PS (**PS-out**). In immunocompetent mice, the engineered PS-out tumours **grew faster**, showing more immunosuppressive/M2-like tumour-associated macrophages (TAMs) and fewer tumour-antigen-specific T cells. Macrophage **TIM-3** was implicated in PS sensing.

The same study generated the opposite condition by removing **XKR8** to limit PS exposure during apoptosis (**PS-in**); tumours grew more slowly, with an experimental **cGAMP -> STING** signal and stronger tumour-antagonistic myeloid/NK responses. The researchers also tested *masking exposed PS* with a soluble PS-binding MFG-E8 C-terminal fragment that lacked its usual signalling-binding portion; it reduced tumour growth in the tested models. That is an example of **changing a signal's interpretation**, not simply increasing PS.

**Do not generalize** a colon cancer mouse model to all pancreatic tumours or senescent cells.

### Equally important counterexample: more PS accompanied greater pancreatic-cancer clearance
A different primary study (Zhao et al., *J Clin Invest* 2025, 135:e193370) found that impairing cancer-cell pyrimidine synthesis (CAD / DHODH / UMPS pathway) under macrophage-produced inflammatory signals depleted tumour UMP, caused greater **surface PS on PI-negative viable/pre-apoptotic pancreatic tumour cells**, and enhanced macrophage engulfment and reduced tumour burden in mouse models. Tumour **CD47 surface abundance did not change**. The authors note that the role of PS itself versus emerging apoptotic cell states requires further analysis.

**Aletheia hypothesis:** The outcome could depend on whether PS exposure signals 'specific defective tumour-cell clearance' or 'chronic immunosuppressive apoptotic mimicry', and on accompanying macrophage cytokines, TIM-3/TAM receptors, CD47/SIRPα, antigen presentation and T-cell state. These differences are testable but the complete unifying mechanism is *not proven*.

### New 2025–2026 reverse-direction research
- A 2025 *PNAS* study implicated **TMEM16F-dependent PS exposure** in immunosuppressive macrophage/TGF-beta signalling. Blocking TMEM16F-dependent PS exposure improved experimental antitumour immunity (context-specific).
- An experimental study indexed in 2026 found that targeting PS-synthesis gene **PTDSS1**, XKR8 or ANO6/TMEM16F can sensitize certain tumours to PD-1 checkpoint blockade. This strengthens the warning that 'more PS outside is always good' is false.
- A recent study indexed in 2026 reported **increased CD47 and surface proteome remodeling in TMEM30A-deficient immune cells**, further undermining any assumption that impairing a flippase only changes PS localization. Do not transfer immune-cell results directly to pancreatic cancer without tests.

### Alternative research strategies that go beyond blocking a protein
1. **Reveal then correctly interpret:** Determine whether tumour PS exposure in a specific model predicts macrophage destruction or suppressive efferocytosis. It is an outcome to measure, not an a priori therapy.
2. **Target PS that is *already exposed*:** Explore tumour-local or tumour-marker-gated PS-binding probes/antibodies or signalling-neutralising adaptors. The 2022 MFG-E8 fragment is a preclinical example; normal activated platelets, apoptotic cells and healthy immune tissues can also display PS, so off-target risks remain.
3. **Rescue productive clearance:** Investigate macrophage and dendritic-cell antigen handling, T-cell priming and inflammatory-versus-resolving states after uptake. A successful 'engulfment' event alone is not proof of durable antitumour immunity.
4. **Production-stage CD47:** Compare QPCTL-dependent surface CD47 maturation and PS externalization as **separate mechanisms** with distinct risks. Mature erythrocytes may be less affected by new protein maturation, but developing red cells and normal nucleated cells remain at risk.

### Minimal evidence-based comparison for future experiments
Compare **surface PS** (e.g. binding assay), **total PS**, **viability/apoptosis**, **ATP11A/C + CDC50A**, **XKR8/TMEM16F activation**, **CD47 abundance and QPCTL-dependent function**, **macrophage uptake and phenotype**, **antigen-specific T-cell activation**, and **normal-cell/platelet toxicity**. Use matched controls and distinguish tumour types; measure both tumour clearance and sustained immune outcomes, including negative results.

### Sources
- **Primary flippase mechanism:** Segawa K et al. (2014). *Caspase-mediated cleavage of phospholipid flippase for apoptotic phosphatidylserine exposure.* Science. https://doi.org/10.1126/science.1252809
- **Independent mechanistic synthesis:** Sakuragi T, Nagata S. (2023). *Regulation of phospholipid distribution in the lipid bilayer by flippases and scramblases.* Nat Rev Mol Cell Biol. https://doi.org/10.1038/s41580-023-00604-z
- **Primary counterexample, colon cancer:** Xue et al. (2022). *Mobilizing phospholipids on tumor plasma membrane implicates phosphatidylserine externalization blockade for cancer immunotherapy.* Cell Reports 41:111582. https://doi.org/10.1016/j.celrep.2022.111582
- **Primary pancreatic cancer positive PS-exposure context:** Zhao et al. (2025). *Targeting plasticity in the pyrimidine synthesis pathway potentiates macrophage-mediated phagocytosis in pancreatic cancer models.* JCI. https://doi.org/10.1172/JCI193370
- **Additional PS immune escape:** Gadiyar V et al. (2025). *Phospholipid scramblases TMEM16F and Xkr8 mediate distinct features of PS externalization and immune suppression to promote tumor growth.* Cell Death Discovery. https://doi.org/10.1038/s41420-025-02789-y
- **2025 TMEM16F immune effect:** Wu M et al. (2025). *TMEM16F phospholipid scramblase regulates tumorigenesis by modulating the tumor immune microenvironment.* PNAS. https://doi.org/10.1073/pnas.2513910122
- **2026 PS resistance to immune checkpoint blockade:** *Suppressing phosphatidylserine externalization overcomes cancer immune evasion and enhances immunotherapy.* PubMed: https://pubmed.ncbi.nlm.nih.gov/42684101/
- **2026 immune-cell membrane / CD47 reorganisation:** *Cell surface remodeling caused by the loss of the flippase subunit TMEM30A in immune cells.* PubMed: https://pubmed.ncbi.nlm.nih.gov/42599021/

EVIDENCE: Primary mechanistic biology and opposing preclinical animal tumour models. No safe selective human PS-exposure manipulation treatment established.

---

## WAR-RESEARCH-001 | Go Walkabout: falsifiable questions

1. **Origin:** In human PDAC specimens, what proportion of IL-18 comes from malignant epithelial cells versus immune/stromal cells, and how does this vary by stage, subtype and KRAS treatment?
2. **Signal:** Is IL-18-induced STAT1/CD47 primarily a tumour-cell-autonomous response, a paracrine circuit, or both? Which receptor/signalling intermediates are necessary?
3. **Macrophage state:** In human pancreatic tumours, how do CD38, SIRPα, MHCII/CD11c, phagocytosis and NAD metabolism co-vary *within defined macrophage subsets*? Do not assume they are one functional state.
4. **Senescence link:** Does senescent-cell SASP change IL-18/CD47 tumour signalling or macrophage phagocytosis in co-culture, organoids or clinically annotated spatial datasets? Treat as a hypothesis until tested.
5. **ROS link:** Can ROS modulate IL-18 processing or CD38-associated inflammatory programmes in a defined model, and can that effect be separated from SASP cytokines and inflammasome activation? This is a question, not a demonstrated common pathway.
6. **KRAS resistance:** What are the timing, magnitude and cell specificity of IL-18 increases during KRAS inhibitor exposure? Do downstream inhibitors of CD47/SIRPα or selective IL-18-axis interventions avoid resistance?
7. **Safety:** Would tumour-local, transient, or tumour-antigen-gated interventions spare normal erythrocyte/platelet CD47 and preserve beneficial NK/T-cell IL-18 responses?
8. **Translation:** Are biomarker-defined human cohorts or interventional trials showing clinical survival benefit, or only preclinical proof of concept? Record negative trials and toxicities as carefully as positive ones.

### Evidence discipline and future work
For each new paper, record date, model/population, cell source, signalling arrow, measured outcome, intervention, adverse effects, evidence grade and a strongest alternative explanation. Maintain separate labels **Established in tested model / Supported association / Aletheia hypothesis / Contradictory evidence / Human clinical evidence**. Update the chain when a new paper contradicts it; don't preserve metaphors at the expense of biology.

## Change log
- **2026-11-19, v0.3.0**: Go Walkabout into PS asymmetry: ATP11A/C, CDC50A/TMEM30A, XKR8 and TMEM16F; added opposing primary tumour outcomes (2022 colon PS-out increased growth vs 2025 pancreatic PS exposure with clearance), 2025–26 immune-suppression research, and revised research tests. No clinical treatment implied.
- **2026-11-18, v0.2.0**: Added non-inhibition strategy, direct 2025 JCI mouse PDAC surface-PS evidence and its immune-suppression counterexamples; QPCTL-dependent CD47 maturation; CD47 long/short mRNA 3'-UTR-dependent localization; CD48 distinction and tumour specificity limits. Not a clinical treatment.
- **2026-11-18, v0.1.0**: Project knowledge branch created. Added the Sun et al. (2026) IL-18 -> STAT1 -> CD47/SIRPα pancreatic cancer mechanism, compared with senescence/SASP -> CD38/NAD+ ageing mechanism, documented IL-18's conflicting roles and CD47 safety constraints, and defined next research tests. No therapy or public app is claimed.
