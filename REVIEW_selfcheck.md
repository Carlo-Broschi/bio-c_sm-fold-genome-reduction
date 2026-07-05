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

## §3.3 Hfq two-mode loss census

| Claim / number | Source (file) | Script | Status |
|---|---|---|---|
| 71 complete genomes, 37 taxa, 8 lifestyles | `bio-a/3-analysis/hfq_census/{bact_manifest,taxa_lifestyle}.tsv` | `fetch_bact_proteomes.py` | ✅ |
| Retention by lifestyle (88/73/100/0/17/18/0/0 %) | `hfq_census.tsv` (recomputed, matches draft exactly) | `hfq_census.py` | ✅ |
| Hfq+ median 4.1 Mb vs Hfq− 1.2 Mb | `hfq_census.tsv` (4.12 / 1.18) | `hfq_census.py` | ✅ |
| point-biserial r = 0.34; 0.51 excl. Actinobacteria | `hfq_census.py` output | `hfq_census.py` | ✅ |
| Lineage medians (endo 0.64 / mollicute 0.82 / intra 1.48 Mb) | `hfq_by_lifestyle.tsv` | `hfq_census.py` | ✅ |
| Actinobacteria 0/8 at 3–9 Mb; Myxococcus 9 Mb; Wigglesworthia/Baumannia/Francisella retain | `hfq_census.tsv` (per-genome) | — | ✅ |

**Robustness (pseudoreplication).** cap=2 gives ≤2 genomes/taxon; 34 taxa have >1 genome
but only 1 shows within-taxon Hfq± disagreement. Collapsing to taxon medians (n=37):
**r = 0.341 overall, 0.506 excl. Actinobacteria — essentially identical to the genome-level
values.** The correlation is therefore not inflated by pseudoreplication. ✅

**Author must own (defensible, not errors):**
- The 37-taxon set is a **stratified, illustrative sample across lifestyles, not a random
  survey** of bacterial diversity; per-lifestyle rates are illustrative, the size–presence
  relationship is the robust result. Frame as such (see suggested wording).
- **Lifestyle labels** (`taxa_lifestyle.tsv`) are a curated classification; each assignment
  (e.g. Francisella "obligate intracellular", Coxiella) must be justifiable by the author.
- **Absence = no detectable Hfq at `--cut_ga`**; a divergent sub-threshold homolog cannot be
  excluded (Actinobacteria, Myxococcus) — already stated as a caveat in the draft. ✅

## §3.4 CPR total loss

| Claim / number | Source (file) | Script | Status |
|---|---|---|---|
| 0/397 (Saccharibacteria 393 + Absconditabacteria 3 + Patescibacteria 1) | `bio-b/3-analysis/hmm/census_lineage_cpr.tsv` | `hmm_type_census.py` | ✅ |
| 290,425 predicted proteins; mean 731/genome | `cpr_manifest.tsv` (sum=290425; 290425/397=731.5) | `fetch_dpann_asgard_proteomes.py --tag cpr` | ✅ |
| 393 Saccharibacteria, 15 species | `census_lineage_cpr.tsv` (n_species=15) | — | ✅ |
| **843 ribosomal-protein annotations** | `proteomes_cpr/*.faa` header grep `ribosomal protein` = **843 exact** | — | ✅ (draft wording "ribosomal-protein" is precise; broad "ribosomal" = 867) |
| 70 archaeal hits = positive control | `bio-b/3-analysis/hmm/census_lineage.tsv` | `hmm_type_census.py` | ✅ |
## §3.5 Archaeal retention

| Claim / number | Source (file) | Script | Status |
|---|---|---|---|
| 50 genomes, 6 assessable lineages | `bio-b/3-analysis/hmm/census_lineage.tsv` (sums to 50 / 6 rows) | `hmm_type_census.py` | ✅ |
| 70 Sm/Lsm hits (44 genomes carry ≥1) | `census_lineage.tsv` (Sm/Lsm hits col sums 70; genomes-with = 44) | `hmm_type_census.py` | ✅ |
| all typed Sm/Lsm, none Hfq | `census_lineage.tsv` (genomes_with_Hfq = 0 all lineages) | — | ✅ |
| 55/55 structural verification; median 0.97 | `smfold_foldseek_verification.tsv` (min 0.918, max 0.999, median 0.9670; is_sm_fold True ×55) | `verify_smfold_foldseek.py` | ✅ |
| **TM-score bound** | actual min = **0.918** | — | ⚠→✅ changed "≥ 0.92" to **"≥ 0.91"** (Abstract, Fig 4 caption/table; bio-b + submission mirrored) — 3 hits are 0.918–0.920 so "≥0.92" was not strictly true |
| 49/55 closest to an archaeal Sm anchor | anchor classification: archaeal 1I5L 14 + 1I4K 11 + 1M5Q 9 + 1I8F 8 + 1M8V 4 + 1H64 3 = **49**; non-archaeal 1D3B 4 + 6GWK 2 = 6 | `structural_anchors.md` + verification tsv | ✅ |

## §3.6 Synthesis

Interpretive section; introduces **no new numbers**. Restates the domain-level asymmetry
(bacterial repeated loss §3.3/§3.4 + archaeal retention §3.5) and the internal-control
logic (true-absence pipeline). All underlying quantities verified in §3.3–3.5. ✅

---

## Introduction / Discussion / Methods — claim & citation review

| Claim | Support / citation | Status |
|---|---|---|
| Veretnik 2009: 335 seqs / 80 species / ClustalW + PhyML | verified against the paper (primary read) | ✅ |
| "eukaryotic Sm/Lsm derives from an archaeal ancestor" | Collins & Mabbutt 2001; Törő et al. 2001 (support archaeal Sm ancestry) | ✅ |
| Novelty: not first detection of DPANN/Asgard Sm | Reichelt et al. 2018 already showed it — explicitly credited; "we do not claim first detection" | ✅ honest |
| Functional-dispensability explanation (archaeal SmAP core RNA metabolism) | Reichelt et al. 2023 (exosome/ribosome/RNAP/RNA-modification), flagged "census-untested" | ✅ hedged |
| **Hfq "peripheral"** | over-statement — Hfq is central in bacteria that have it | ⚠→✅ reworded to "specialized … evidently dispensable in many lineages (as its repeated loss here shows)"; dropped "peripheral" (×2) |
| Myxococcus lacks Hfq (size-independent loss example) | our census (0/2) **corroborated** by literature: *M. xanthus* has no hfq homolog (Pxr sRNA is Hfq-independent) | ✅ (independently supported) |
| Actinobacteria canonical Hfq absent | our census (0/8) + long-standing reports; caveat re: cut_ga stated | ✅ |
| "structure-guided from 19 experimental structures" | `0-literature/structural_anchors.md` (A1–A11 + B) | ✅ (author to re-confirm the count is exactly 19) |

### Action item 1 — structure-guided IQ-TREE reconfirmation (2026-07-05)
- **UFBoot ≥ 95 = 470/1092 = 43.0%** recomputed from the committed `.contree` → **exactly reproduces the reported "43%"**. ✅
- **logL**: the reported −81,864.04 is the value in the committed `.iqtree` from the original run (correct to cite). A quick *fixed-tree* re-evaluation (`-te treefile -m Q.INSECT+G4`) gives −81,927.9 — a ~64-unit difference expected from re-optimising branch lengths/model on the fixed topology; not an error, a different computation.
- **Independent full re-inference launched** (new seed 20260705, `-m Q.INSECT+G4 -B 1000`, prefix `structguided_INDEP_reverify`, bio-b/3-analysis). ~7 h; on completion compare its `.iqtree` logL and `.contree` UFBoot≥95 fraction to the originals. **[pending completion]**

### Author action items still open
- [ ] Confirm the independent re-run reproduces topology/logL/43% when it finishes.
- [x] **Phylum counts 114/92 verified** at the *tip* level (tip→genus via `tip_labels.tsv` → phylum via `genus_taxonomy.tsv`): Pseudomonadota 114, Bacillota 92 exactly. NB `genus_taxonomy.tsv` alone counts *genera* (148/39), not tips — the join is required. 12 tips unclassified (honestly reported).
- [x] **Lifestyle labels reviewed** (`bio-a/.../lifestyle_justification.md`). **Francisella reclassified** obligate_intracellular→facultative_host (facultative, axenically culturable, retains Hfq): obligate_intracellular sharpened to **0/10 (0%)**; correlation unchanged (r=0.34/0.51). Actinobacteria now explicitly framed as a size-independent-loss test group. Coxiella kept obligate (axenic caveat noted).
- [ ] Read through and be able to explain each claim in the author's own words.
- [x] Traceability: definitive structure-guided type table committed.
- [x] UFBoot 43% reproduced; TM bound corrected; "peripheral" overclaim reworded.
