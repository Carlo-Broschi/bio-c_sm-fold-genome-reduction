# Critical peer review — bio-c (*The fate of the Sm fold under genome reduction*)

**Reviewer stance:** critical GBE referee, first read of the final integrated manuscript. **Scope:** verification and critical review, not rewriting. **Restriction:** only NEW issues beyond those already resolved in `REVIEW_selfcheck.md` are reported; areas that pass are noted briefly. All numbers were recomputed independently from the data files in `bio-c/3-analysis/`, `bio-a/3-analysis/hfq_census/`, and `bio-b/3-analysis/hmm/` + `4-results/` — the draft text and the self-check were treated as claims to test, not as ground truth.

## Verdict

The manuscript is quantitatively sound: **every headline number reproduces exactly from the data files** (details in §Numbers below), all 39 references resolve to correct DOIs, all six figures match their captions and the recomputed values, and the statistics and hedging are appropriate. The novelty positioning is honest. No blocker- or major-severity scientific error was found. The findings below are one **major** documentation gap (a referenced supplementary table that does not exist), a small set of **minor** presentation/consistency issues, and one item I could not verify from this environment. None requires a change to the science.

---

## Findings (severity-ranked)

### MAJOR

**M1 — Referenced "Supplementary Table S1" does not exist in the repository.**
*Location:* §2.3 ("19 experimentally determined Sm-fold structures … PDB accessions in Supplementary Table S1"), §2.7 (structural anchors), Data Availability ("Protein and genome accessions are listed in the supplementary material").
*Problem:* No `Table S1` / supplementary accession file is present anywhere in the repo (only `FigS1`). The 19-structure anchor list and the protein/genome accession tables are load-bearing for reproducibility and are promised in three places, but a reviewer cannot open them. As it stands the manuscript cites a display item it does not provide.
*Fix:* Prepare Supplementary Table S1 (the 19 anchor PDB IDs with organism/domain, plus the census accession tables) and include it in the submission package; or, if the accessions live only in the code repo, change the wording to point at the specific repository file rather than a supplementary table. The underlying data exist (`bio-b/0-literature/structural_anchors.md` lists the anchors; `cpr_manifest.tsv`, `hfq_census.tsv` carry accessions) — this is a packaging gap, not a data gap.

### MINOR

**m1 — Reference-list count in the draft is stale ("26 entries").**
*Location:* end of `draft.md` References section — both the HTML comment (`最終リストは REFERENCES_gbe_final.md（26件）`) and the visible line "See `REFERENCES_gbe_final.md` (26 entries, GBE author–date, DOI-verified)."
*Problem:* The final list has **39** entries, not 26. A leftover from an earlier draft.
*Fix:* Change "26" → "39" in both places (and note that these are internal scaffolding lines that should be stripped at submission anyway).

**m2 — §2.3 "dereplicated … into a 25-sequence structural seed" reads as an arithmetic contradiction.**
*Location:* §2.3: "19 experimentally determined Sm-fold structures … dereplicated at 95% identity with CD-HIT into a 25-sequence structural seed."
*Problem:* Dereplication (CD-HIT) can only *reduce* sequence count, so 19 → 25 is impossible as literally written. The intended meaning is presumably that per-chain sequences were extracted from the 19 multi-chain heptameric/hexameric assemblies (well over 25 chains) and then dereplicated to 25. As written it will read as an error to a careful referee.
*Fix:* Add one clause, e.g. "chains extracted from the 19 assemblies were dereplicated at 95% identity with CD-HIT into a 25-sequence structural seed."

**m3 — Two in-text citations use "&" (two-author form) for papers with >2 authors.**
*Location:* "Collins & Mabbutt 2001" (Introduction, Discussion) and "Payá & Bonete 2023" (§3.5).
*Problem:* The manuscript's own stated style is ">2 authors → first author + et al." Collins et al. 2001 has 6 authors (Collins, Harrop, Kornfeld, Dawes, Curmi, Mabbutt) and Payá et al. 2023 has 5 (Payá, Bautista, Camacho, Esclapez, Bonete). Both in-text forms cite the *last* author as if second of two. (The reference-list entries themselves are correct.)
*Fix:* "Collins et al. 2001" and "Payá et al. 2023" in the running text. ("Moran & Bennett 2014" is correct — genuinely two authors.)

**m4 — Stale committed derived file `bio-c/3-analysis/hfq_by_lifestyle.tsv` contradicts the draft.**
*Location:* repo file `3-analysis/hfq_by_lifestyle.tsv`.
*Problem:* This file holds *pre-reclassification* values (obligate intracellular 2/12 = 17 %, facultative/host 8/11) that contradict the draft text and Fig 3A (obligate intracellular 0/10 = 0 %, facultative 10/13). The draft and figure are built from the authoritative per-genome `bio-a/.../hfq_census.tsv` and are **correct**; the committed lifestyle-summary TSV was simply not regenerated after Francisella was moved from obligate-intracellular to facultative. It is an unused orphan, but it will confuse anyone who opens it to check the census.
*Fix:* Regenerate `hfq_by_lifestyle.tsv` from the final `hfq_census.tsv`, or remove it, so the committed derived file agrees with the manuscript.

**m5 — DPANN/Asgard "nine lineages + five classes" (=14) never reconciled with the 6 assessable lineages reported.**
*Location:* §2.6 ("DPANN (nine lineages) and Asgard (five classes)") vs §3.5 / Table 1 (six lineages).
*Problem:* The data-insufficient *rule* is stated, but the manuscript never says how many of the 14 sampled groups were dropped for want of a completeness-passing genome (8), so a reader cannot reconcile "nine + five" with the six rows in Table 1.
*Fix:* Add a half-sentence, e.g. "of the fourteen sampled groups, six had ≥1 completeness-passing genome and are reported here; the remaining eight are data-insufficient."

**m6 — Point-biserial correlation reported without p-value, CI, or n at the point of claim.**
*Location:* §3.3 ("point-biserial r = 0.34; r = 0.51 with the Actinobacteria excluded").
*Problem:* This is described as "the robust quantitative result," yet only the coefficient is given. Recomputation confirms it is significant (r = 0.342, p = 3.5 × 10⁻³, 95 % CI 0.12–0.53, n = 71), so this is a reporting-completeness point, not a correctness one.
*Fix:* Add p and/or 95 % CI (and n) once, so the headline statistic is fully specified.

**m7 — "Reichelt et al. 2018 indicated qualitatively" slightly undersells the prior work.**
*Location:* §3.5 and Discussion ("Novelty and prior work").
*Problem:* The 2018 review (ref #26) reports an EFI sequence-similarity analysis of ~999 archaeal Lsm-domain proteins that already places SmAP in DPANN and Asgard groups — more than a "qualitative" indication. The manuscript's genuinely distinct contributions (completeness-controlled MAG census, structural verification, the CPR contrast) are real and correctly claimed, so this does not threaten novelty, but the word "qualitatively" is a slight mischaracterisation that an informed referee (or the Reichelt group) may notice.
*Fix:* "previously reported by sequence analysis (Reichelt et al. 2018)" or similar, rather than "qualitatively."

**m8 — Fig 3A colour key not explained in the caption.**
*Location:* Fig 3A (obligate-endosymbiont bar is red; all other bars blue) and its legend.
*Problem:* The single red bar clearly encodes something (the one reduced-lifestyle category that still retains Hfq in a minority of genomes, 18 %), but the caption does not say what the colour means.
*Fix:* One clause in the Fig 3 legend explaining the red/blue distinction, or make all bars one colour.

### COULD NOT VERIFY (advisory, not a finding)

**v1 — Repository public status and Zenodo record publication.**
`doi.org` and `github.com` are not reachable from the review environment, so I could not confirm that the GitHub repo is actually **public** or that the three Zenodo DOIs (bio-c 10.5281/zenodo.21202213; bio-a …21197822; bio-b …21197824) resolve to **published** records rather than reserved-but-unpublished drafts. Reproducibility and the companion cross-links depend on this. Please confirm all four are live and public before submission. (This mirrors the standing advisory on the companion bio-a/bio-b repositories.)

---

## Areas checked and passing (no new issue)

- **Citations / DOIs.** All 39 reference entries are cited in-text; every in-text citation resolves to a list entry (no orphans, no missing). All 39 DOIs verified against CrossRef/OpenAlex and resolve to the correct work. *Note:* ref #26 Reichelt 2018 DOI `10.1042/etls20180034` is **correct** (it resolves to "A journey through the evolutionary diversification of archaeal Lsm and Hfq proteins"); a plausible-looking neighbour `…20180023` is a different (CRISPR) paper, so the author chose the right one. The five recently-added positioning citations (Kim 2025, Srinivas 2024, Li 2025, Payá 2024, McCutcheon 2024) and the DPANN/Asgard/CPR foundational set (Rinke 2013, Spang 2015, Zaremba-Niedzwiedzka 2017, Imachi 2020, Brown 2015, Castelle & Banfield 2018) all support the claims they are attached to.
- **Numbers (independently recomputed, all reproduce exactly).** Census 71 genomes / 37 taxa / 8 lifestyles; Hfq-present median 4.12 Mb vs absent 1.16 Mb; point-biserial r = 0.342 (0.511 excl. Actinobacteria); taxon-median r = 0.339 / 0.506; per-lifestyle rates (free-living 88 %, facultative 77 %, endosymbiont 18 %, obligate intracellular 0/10, mollicute 0/6, spirochete 0/4, Actinobacteria 0/8, Aquificota 3/3); obligate-intracellular median 1.18 Mb; CPR 0/397 (290,425 predicted proteins, 843 ribosomal-protein annotations, Saccharibacteria 393 genomes / 15 species); archaea 50 genomes / 6 assessable lineages / 70 Sm-Lsm hits / 0 Hfq, with Table 1 per-lineage hit counts (Asgard 24, Loki 20, Nano 14, Micr/Nanohalo/Parv 4 each) all matching; structural verification 55/55, min TM 0.918, median 0.967 (→ "0.97"), 49/55 closest to an archaeal anchor; bacterial Hfq tree 225 taxa / 254 sites / 139 parsimony-informative, Q.INSECT+I+G4, logL −17,597.4, ML–Bayes congruence 86/91 = 94.5 %, PP median 0.92, 36/86 PP ≥ 0.95, 5/5 outgroup monophyletic; phyla 114 Pseudomonadota / 92 Bacillota; structure-guided tree 1,101 × 184, Q.INSECT+G4, logL −81,864.04, 470/1,092 = 43.0 % UFBoot ≥ 95 (non-converged). *(The self-check's parenthetical "obligate intracellular 1.48 Mb" is a slip in the self-check only; the draft's 1.18 Mb is the correct median.)*
- **Figures vs captions.** All six match. Fig 1 (fan tree, colour-blind-safe type palette; the earlier stale in-plot "1097 tips" title is gone). Fig 2 (225-taxon rooted ML tree, ML/Bayes concordance dots, only the 5 outgroup taxa labelled — legible at column width). Fig 3 (built from the correct post-reclassification data — the stale TSV of m4 did **not** propagate to the figure; 3B size-independent diamonds at 2–9 Mb). Fig 4 (retention/loss bars + TM histogram "all 55 ≥ 0.91, median 0.97"). Fig 5 (superposition on PDB 1I4K at TM 0.97 — substantiated; real 1I4K-anchored hits at exactly 0.970 exist). Fig S1 (phylum-coloured tree, consistent with 114/92).
- **Methods reproducibility.** Tool versions and parameters are stated and internally consistent (IQ-TREE3 v3.1.3, MrBayes 3.2 with VT+G4 fixed, CD-HIT v4.8.1, MAFFT v7, HMMER v3.4 `--cut_ga`, Foldseek v10, Prodigal, RogueNaRok, NCBI Datasets v2); the model names in the text match the `.iqtree` files; and the sequence-processing arithmetic (500 → 293 → 229 → +5 → −9 rogues → 225 = 220 Hfq + 5 SmAP) is fully consistent. (Two clarity items are m2 and m5 above.)
- **Statistics.** Point-biserial is the correct binary-vs-continuous coefficient; the pseudoreplication (taxon-median) robustness check reproduces and is honestly reported; sample sizes (n = 71/37, 12 unclassified tips, 6-of-14 assessable lineages) are stated transparently. (Reporting completeness is m6.)
- **Over-claims / logic.** The hedges the task flags are all present and adequate: the `--cut_ga` "detectable canonical Hfq" caveat, the stratified-sample framing, the "census-untested" label on the functional-dispensability hypothesis, and the CPR "first assessment" wording. Archaeal retention is stated at the lineage level and Fig 4A shows the per-genome fractions (44/50 carry the fold) transparently, so "retained in every quality-genome lineage" is defensible.
- **Novelty positioning.** First detection of archaeal Sm/Lsm is explicitly *not* claimed (Reichelt 2018 and Payá 2023 credited); the CPR "first assessment" is defensible against the current literature (an independent 2020–2026 search found no Hfq/Sm census in any CPR lineage, and Srinivas 2024 reviews CPR biology without addressing these proteins). (The "qualitatively" wording is the minor m7.)
- **COPE / ethics.** The AI-use disclosure is thorough, honest and task-scoped (names the tool, lists the assisted steps, author takes full responsibility, AI not listed as author, cites COPE guidance); competing interests are declared; Data Availability lists the GitHub repo, the bio-c Zenodo DOI, and both companion Zenodo cross-links, plus an accession pointer. (Textually complete; the live-status caveat is v1 and the missing supplementary table is M1.)

---

*Method note.* Numbers were recomputed in an independent Python environment (dendropy/biopython/pandas/scipy) directly from the primary files — `hfq_census.tsv` (point-biserial, medians, per-lifestyle rates, taxon-median collapse), `census_lineage{,_cpr}.tsv` and `hits_all.tsv` (archaeal/CPR counts), `cpr_manifest.tsv` and a header grep of the 397 CPR proteomes (290,425 proteins; 843 ribosomal), `smfold_foldseek_verification.tsv` (TM distribution and anchors), the bio-a `.iqtree`/`.contree` and `ml_bayes_comparison.txt` with a `tip_labels`→`genus_taxonomy` join (Hfq-tree stats, congruence, phyla), and the bio-b structure-guided `.iqtree`/`.contree` (1,101×184, logL, 43 %). DOIs were checked against CrossRef and OpenAlex. All six figure images were opened and compared panel-by-panel against captions and the recomputed values.
