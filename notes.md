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

26 entries merged from bio-a (11) ∪ bio-b (23), 8 shared. See `REFERENCES_gbe_final.md`
and `refs.bib`. All in-text citations resolve to a list entry (checked 2026-07-05).

## Status / next steps

- [x] Folder + figures + merged refs + metadata (CITATION.cff, .zenodo.json, LICENSE CC-BY-4.0)
- [x] Integrated draft.md (framework + Finding 1 bacteria + Finding 2 archaea + synthesis)
- [ ] git init + push + Zenodo (offered)
- [ ] Table 1 rendered content (copy from bio-b) into draft
- [ ] Compliance check (word/char/item counts vs GBE) and preprint PDF
- [ ] Retire bio-a/bio-b as standalone submissions (keep repos as archived components)
