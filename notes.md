# bio-c Assembly Notes — integrated Sm-fold study

**Author:** Minoru Nakai
**Created:** 2026-07-05

## Provenance

bio-c consolidates two QC-locked companion analyses into a single integrated
manuscript (decision: integrate rather than submit two thin companion papers,
to avoid a salami-slicing concern given the shared reciprocal-outgroup design
and shared census methodology).

| Source | Contributed to bio-c |
|---|---|
| bio-a (Hfq) | Rooted dual-method Hfq phylogeny (§3.2, Fig 2/2b); **new** Hfq-loss census (§3.3, Fig 3); ESMFold/Foldseek tip verification |
| bio-b (Sm/Lsm) | Curated superfamily dataset (§3.1); structure-guided 3-domain tree (§3.2, Fig 1); CPR loss (§3.4); DPANN/Asgard retention + structural verification (§3.5, Fig 4, Table 1); functional-dispensability argument (Reichelt 2023) |
| **new (bio-c)** | Integrated framing (framework + two findings + synthesis); §3.3 two-mode Hfq-loss census; §3.6 domain-level asymmetry synthesis |

## Key numbers (carried from the QC-locked sources)

- Bacterial Hfq tree: 225 taxa, 254 sites (139 parsimony-informative), ML/Bayes congruence 86/91 (94.5%).
- **Hfq-loss census (new): 71 complete genomes, 8 lifestyles.** Hfq+ median 4.1 Mb vs Hfq− 1.2 Mb; point-biserial r=0.34 (0.51 excl. Actinobacteria). Free-living 88%, Aquificota 100%, Actinobacteria 0/8 (3–9 Mb), Myxococcus 0 (9 Mb), mollicute 0%, endosymbiont 18%, intracellular 17%, spirochete 0%.
- CPR: 0/397 (393 Saccharibacteria, 290,425 proteins, 843 ribosomal).
- DPANN/Asgard: 50 genomes / 70 hits / 6 lineages; 55/55 structural verification, TM median 0.97, 49/55 archaeal-anchor.

## Reference set

Merged from bio-a (11) ∪ bio-b (23), 8 shared = 26 baseline; expanded to 39 entries
(2026-07-05) after the GBE benchmark + novelty/scoop check added 8 foundational + 5
positioning citations; **further expanded to 48 entries (2026-07-07)** by adding 9
structural/evolutionary Sm/Lsm/Hfq references surfaced in an Obsidian score≥8
citation-gap check (Arluison 2006, Murina & Nikulin 2011, Mura 2013, Stanek 2017,
Wilusz 2013, Krchňáková 2017, Lekontseva 2020/2021, Mu 2025) — each CrossRef-verified
and given an in-text anchor (Intro structural/function/spliceosome-evolution paras; §3.5).
See `REFERENCES_gbe_final.md` and `refs.bib`. All in-text citations resolve to a list entry.

## Status / next steps (updated 2026-07-05)

- [x] Folder + figures + merged refs (26) + metadata (CITATION.cff, .zenodo.json, LICENSE CC-BY-4.0)
- [x] Integrated draft.md (framework + Finding 1 bacteria + Finding 2 archaea + synthesis)
- [x] git init + push + **Zenodo DOI 10.5281/zenodo.21202213** (recorded in Data Availability/README)
- [x] Table 1 rendered; Fig 2b → Supplementary Fig S1; GBE compliance all pass; preprint PDF built
- [x] bio-a/bio-b marked archived components (README notes + reciprocal DOIs); not submitted independently
- [x] **COPE AI-use disclosure + competing-interests** added (Declarations)
- [x] **Comprehensive author self-check (approach A)** — see `REVIEW_selfcheck.md`. All §3.1–3.6 + Intro/Disc/Methods numbers traced to source; fixes: type-table traceability, TM ≥0.92→≥0.91, "peripheral" overclaim, stratified-sample framing.
- [x] **Francisella reclassified** obligate_intracellular→facultative_host → obligate intracellular now 0/10; Actinobacteria framed as size-independent test group.
- [x] Phylum 114/92 verified at tip level; Myxococcus Hfq-absence corroborated by literature.
- [x] **GBE benchmark + expansion (2026-07-05)**: refs 26→39, body ~2,600→~4,400 words; Methods/Intro/Discussion expanded; figures made colour-blind-safe (Okabe-Ito), titles removed, Fig 2 legibility, **structure Fig 5 + Supplementary Table S1 (19 anchors) added**.
- [x] **Novelty/scoop check** (positioning citations added) and **final background peer review** — no scientific blocker/major; Supplementary Table S1 + 8 minor findings resolved.
- [x] **Two submission-format versions built** (`submission/gbe/`, `submission/jme/`, both PDF, in git). JME references verified against a real recent JME article → first-3-authors-+"et al" (no period), "Conflict of interest" heading. **Strategy: submit to JME first (no APC via subscription route), GBE if rejected.**
- [x] **Citation-gap expansion (2026-07-07)**: a score≥8 check against the Obsidian bio-c note library (194 notes; 178 unique after `duplicate_of:` tagging of 16 redundant notes) surfaced 9 uncited on-topic structural/evolutionary refs. All DOIs CrossRef-verified and each given an in-text anchor (Intro structural/function/spliceosome-evolution paragraphs; §3.5 archaeal retention) so no orphan references. refs **39→48** across refs.bib, both reference lists, and both submission manuscripts' embedded lists (existing alphabetical order preserved). Added: Arluison 2006, Murina & Nikulin 2011, Mura 2013, Stanek 2017, Wilusz 2013, Krchňáková 2017, Lekontseva 2020/2021, Mu 2025. PDFs regenerated.
- [!] **Git incident + fix (2026-07-07)**: a `git add -A` accidentally committed the untracked local `refs/` PDF library (53 copyrighted publisher PDFs) to the public repo. Corrected: untracked + `.gitignore`d, then **purged from all history with `git-filter-repo` and force-pushed** (paths 0 across history). PDFs remain locally, ignored. Lesson: stage explicitly here, never `git add -A`. Note: old commit SHAs may stay cached on GitHub until server-side GC.

### Author action items still open (COPE accountability — author must own)
- [~] Independent structure-guided IQ-TREE re-run: **UFBoot 43% reproduced exactly**; full re-inference running (bg watcher), confirm logL/topology on completion.
- [ ] Read through draft; be able to explain each claim in own words.
- [ ] (optional) confirm Coxiella obligate-vs-facultative call.

### Remaining before submission (author, when funds available)
- bioRxiv upload (`_biorxiv/bioc_preprint.pdf`); GBE/MBE submission (CMYK TIFF at upload); Zotero-formatted refs.
