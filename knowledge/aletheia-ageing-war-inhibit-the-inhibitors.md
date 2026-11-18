# Aletheia Ageing War: Inhibit the Inhibitors

Status: KNOWLEDGE-ONLY / RESEARCH PROJECT / NOT TREATMENT ADVICE  
Version: 0.1.0  
Created: 18 November 2026  
Last evidence review: 18 November 2026  
Scope: cellular senescence, inflammatory signalling, macrophage reprogramming, NAD metabolism, immune evasion, pancreatic cancer, and the risks of indiscriminate inhibition.  
Project principle: **Find the pathological brake, identify who is pressing it, and preserve the healthy brakes.**

> This public file records research hypotheses and independently attributable findings. It is neither a cancer-treatment protocol nor an instruction to use medicines, supplements or unapproved interventions. It contains no personal health information.

## Philosophy: the internal war is not simply good cells against bad cells

Many biological signals have two or more roles. A protective signal may be hijacked by diseased cells; a normal immune reaction may contribute to age-related metabolic dysfunction; a molecule that blocks immune attack in one context can stimulate it in another.

**Inhibit the inhibitors** is an *investigation framework*, not a rule to inhibit everything marked inhibitory. The research sequence is:

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
- **2026-11-18, v0.1.0**: Project knowledge branch created. Added the Sun et al. (2026) IL-18 -> STAT1 -> CD47/SIRPα pancreatic cancer mechanism, compared with senescence/SASP -> CD38/NAD+ ageing mechanism, documented IL-18's conflicting roles and CD47 safety constraints, and defined next research tests. No therapy or public app is claimed.
