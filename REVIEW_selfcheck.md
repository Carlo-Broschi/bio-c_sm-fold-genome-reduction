# bio-c — Author self-check / traceability (COPE accountability review)

Comprehensive section-by-section review (approach A): for every claim, the number's
source file and the generating script are recorded so the author can independently
vouch for and defend the content. ✅ = verified against source; ⚠ = issue found/fixed.

## §3.1 A curated, contamination-controlled superfamily dataset

| Claim / number | Source (file) | Script | Status |
|---|---|---|---|
| 6,103 initial retrieval | `bio-b/1-downloaded-data/smlsm_all.fasta` | `fetch_smlsm.py` | ✅ |
| ~15% contamination | nr70 colour-coded tree diagnosis | (2026-07-03 curation) | ✅ (qualitative) |
| 5,665 curated | `bio-b/2-preprocessed-data/smlsm_all_curated.fasta` (grep -c ">" = 5665) | `filter_contaminants.py` | ✅ |
| 1,107 representatives (CD-HIT nr90) | CD-HIT nr90 output | CD-HIT step | ✅ |
| 1,101 analysis-alignment sequences = tree tips | `smlsm_tree_structguided.iqtree` ("1101 sequences") | IQ-TREE3 | ✅ |
| Type counts Hfq 231 / SmAP 27 / Lsm 498 / Sm-core 335 / Other 10 (=1101) | **`biob_tip_types_structguided.tsv`** (written 2026-07-05) | `build_biob_types.py` + structure-guided tree | ✅ (see note) |

**⚠→✅ Traceability fix (2026-07-05).** The committed `biob_tip_types.tsv` (1,097 tips,
Lsm 499 / Other 5) is built from the *plain* curated alignment, not the structure-guided
tree the paper presents. The draft's per-type counts (498 Lsm, 10 Other, summing to 1,101)
are correct for the **structure-guided tree** (Fig. 1), verified by mapping the type table
onto the 1,101 structure-guided tips (Lsm 498, Sm-core 335, Hfq 231, SmAP 27, Other 10).
A definitive per-tree table `biob_tip_types_structguided.tsv` was written so the §3.1
numbers trace directly to a committed file. No science changed; the manuscript numbers
were already correct.

## §3.2 Framework + dual-method Hfq phylogeny

| Claim / number | Source (file) | Script | Status |
|---|---|---|---|
| Structure-guided tree 1,101 × 184, Q.INSECT+G4, logL −81,864 | `smlsm_tree_structguided.iqtree` | IQ-TREE3 | ✅ |
| 43% UFBoot≥95, non-converged | `smlsm_tree_structguided.iqtree` / `.contree` | IQ-TREE3 | ✅ (recompute pending independent re-run) |
| Plain-alignment control 48% | prior bio-b run | IQ-TREE3 | ✅ |
| Hfq tree 225 taxa, 254 sites, 139 parsimony-informative | bio-a alignment / `.iqtree` | IQ-TREE3 | ✅ |
| ML/Bayes congruence 86/91 (94.5%), PP median 0.92, 36/86 PP≥0.95 | `bio-a/4-results/ml_bayes_comparison.txt` | `compare_ml_bayes.py` | ✅ |
| SmAP outgroup 5/5 single bipartition | `ml_bayes_comparison.txt` ("外群 taxon 検出: 5/5") | `compare_ml_bayes.py` | ✅ |
| Phyla Pseudomonadota 114 / Bacillota 92 | `bio-a/4-results/genus_taxonomy.tsv` | `build_taxonomy.py` | ✅ (to re-confirm) |
| 10/10 tip structural verification | `bio-a/4-results/bioa_verify_foldseek.tsv` | `predict_verify_targets.py` | ✅ |

## §3.3 Hfq two-mode loss census  — PENDING (next)
## §3.4 CPR total loss  — PENDING
## §3.5 Archaeal retention  — PENDING
## §3.6 Synthesis  — PENDING

---

### Author action items surfaced by the review
- [ ] Independently re-run the structure-guided IQ-TREE to reconfirm 43%/logL (marked "pending" in prior QC).
- [ ] Re-confirm phylum counts (114/92) from `genus_taxonomy.tsv`.
- [x] Traceability: definitive structure-guided type table committed.
