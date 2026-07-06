# The fate of the Sm fold under genome reduction (bio-c)

**Project ID:** bio-c (integrated) · **Status:** Draft assembly (2026-07)
**Target journal:** Genome Biology and Evolution / Molecular Biology and Evolution
**Author:** Minoru Nakai — Independent Researcher

## Overview

An integrated study of the Sm/Lsm/Hfq superfamily that unifies two earlier
companion analyses (bio-a: bacterial Hfq phylogeny; bio-b: Sm/Lsm three-domain
census) into a single narrative: **how the Sm fold fares under genome reduction
across the three domains of life.**

The paper is organised as a phylogenetic *framework* plus two comparative
*findings*:

- **Framework** — a structure-guided three-domain phylogeny of the whole
  superfamily, plus a rooted, dual-method (ML + Bayesian) bacterial Hfq phylogeny.
- **Finding 1 (bacteria)** — Hfq presence/absence across 71 complete bacterial
  genomes spanning eight lifestyles shows Hfq loss tracks genome reduction, but in
  **two modes**: reduction-associated loss (endosymbionts, mollicutes, obligate
  intracellular) *and* size-independent lineage loss (Actinobacteria, Myxococcus).
  The bacterial CPR radiation has lost the fold entirely (0/397).
- **Finding 2 (archaea)** — DPANN/Asgard archaea retain the Sm fold (55/55 hits
  structurally verified), in contrast to the bacterial losses.
- **Synthesis** — a domain-level asymmetry in Sm-fold fate under genome reduction,
  with a functional-dispensability explanation.

## Provenance

Consolidated from the two companion repositories:
- `bio-a_hfq-phylogenetics` — Hfq dual-method phylogeny + Hfq-loss census
- `bio-b_sm-lsm-phylogenetics` — Sm/Lsm three-domain tree + DPANN/Asgard/CPR census

Raw intermediate data remain in those repositories; this repository holds the
integrated manuscript, final figures, merged reference set, and the analysis
scripts needed to reproduce the consolidated results.

## Structure

| Path | Contents |
|------|----------|
| `4-results/` | Final figures (Fig 1–5 + Fig S1) |
| `scripts/analytics/` | Census / comparison scripts (Hfq census, HMM census, ML/Bayes compare) |
| `scripts/viz/` | Figure scripts |
| `3-analysis/` | Key census result tables |
| `draft.md` | Integrated manuscript |
| `REFERENCES_gbe_final.md` | Merged 48-entry GBE reference list |
| `refs.bib` | Merged BibTeX (Zotero import) |
| `notes.md` | Assembly log and provenance |

## Data and code availability

Archived at Zenodo: doi:10.5281/zenodo.21202213 (this study); companion analyses doi:10.5281/zenodo.21197822 (bio-a) and doi:10.5281/zenodo.21197824 (bio-b).

## Author

Minoru Nakai — Independent Researcher
Email: vivaldi.rv484@gmail.com
