# The fate of the Sm fold under genome reduction: a structure-informed phylogeny across the three domains of life — Manuscript Draft

**Project:** bio-c — integrated Sm/Lsm/Hfq study
**Author:** Minoru Nakai
**Target journal:** Genome Biology and Evolution / Molecular Biology and Evolution
**Status:** Draft assembly (2026-07); integrates the QC-locked bio-a (Hfq) and bio-b (Sm/Lsm) analyses plus a new bacterial Hfq-loss census.

---

## Abstract

The Sm/Lsm/Hfq superfamily builds the RNA-associated toroidal rings that underlie processes from eukaryotic pre-mRNA splicing to bacterial small-RNA regulation, and its distribution across the three domains bears on the archaeal ancestry of the eukaryotic spliceosome. Building a structure-guided three-domain phylogeny of the superfamily and a rooted, dual-method (maximum-likelihood and Bayesian) phylogeny of the bacterial Hfq family, we ask how the Sm fold has fared under genome reduction in each domain. In bacteria, a completeness-controlled census of Hfq across 71 complete genomes spanning eight lifestyles shows that Hfq loss tracks genome reduction (Hfq-present genomes median 4.1 Mb versus 1.2 Mb for Hfq-absent) but follows two distinct modes: reduction-associated loss in endosymbionts, mollicutes and obligate intracellular bacteria, and size-independent lineage loss in the Actinobacteria (3–9 Mb genomes, none with detectable Hfq) and Myxococcus. The bacterial CPR/Patescibacteria radiation has lost the fold entirely (0/397 quality genomes). In sharp contrast, reduced-genome archaea (DPANN, Asgard) retain the Sm fold in every quality-genome lineage examined, with all 55 confidently modelled hits matching an experimental Sm-fold anchor (TM-score ≥ 0.92). The Sm fold thus shows a domain-level asymmetry in its fate under genome reduction — repeatedly lost across bacteria yet retained across reduced-genome archaea — a contrast we draw rigorously and interpret in terms of the differing functional dispensability of the fold in the two domains.

---

## Significance statement

The Sm/Lsm/Hfq fold builds RNA-associated rings found across all cellular life, and its fate in reduced-genome lineages informs the archaeal origin of the eukaryotic spliceosome. Using a structure-guided phylogeny and completeness-controlled, structurally-verified censuses, we show that the fold is repeatedly lost across bacteria under genome reduction — and, independently, in whole lineages such as the Actinobacteria — yet is retained across reduced-genome archaea (DPANN, Asgard). This domain-level asymmetry, drawn rigorously here, separates genuine gene loss from detection and assembly artifacts and points to a functional-dispensability basis for the divergent fates of a single ancient fold.

---

## 1. Introduction

### Background

The Sm/Lsm protein family is one of the most ancient and conserved families in the history of life. In eukaryotes, seven Sm proteins (SmB, SmD1, SmD2, SmD3, SmE, SmF, SmG) and eight Lsm proteins (Lsm1–Lsm8) form heptameric rings that associate with snRNAs to constitute the spliceosome and mRNA-decay machinery. Archaeal homologs (Sm-like archaeal proteins, SmAP) form similar homomeric rings involved in RNA binding, and the bacterial counterpart Hfq shares the same Sm fold — an N-terminal α-helix over a strongly bent five-stranded antiparallel β-sheet (Sm1 motif, β1–β3; Sm2 motif, β4–β5) — despite low sequence identity, assembling into a homohexameric ring rather than a heptamer. The evolutionary relationships among these proteins across the three domains bear on the early evolution of the spliceosome (Veretnik et al. 2009) and on eukaryogenesis, since the eukaryotic Sm/Lsm machinery is thought to derive from an archaeal ancestor.

### Gap

The most comprehensive phylogenetic study of the Sm/Lsm family to date (Veretnik et al. 2009) analysed 335 sequences from 80 species using ClustalW alignment and PhyML. In the intervening ~17 years, sequence data have grown by more than an order of magnitude, phylogenetic methods have advanced (structure-guided alignment, ModelFinder, ultrafast bootstrap, Bayesian inference with convergence diagnostics), and — critically — the reduced-genome radiations that dominate the two prokaryotic domains have become sampled: the archaeal superphyla **DPANN** and the eukaryote-related **Asgard** archaea, and the bacterial **CPR/Patescibacteria**. How the Sm fold has fared under the genome reduction that characterises these radiations, and whether that fate differs between bacteria and archaea, has not been examined with modern, completeness-controlled, structurally-verified methods. Low-sensitivity searches confound true loss with failure to detect divergent sequences, and metagenome-assembled genomes confound absence with incomplete assembly.

### Aims

This study is organised as a phylogenetic *framework* plus two comparative-distribution *findings*.

1. **Framework** — to place the Sm/Lsm/Hfq superfamily in an updated, structure-guided three-domain phylogeny, and to reconstruct a rooted, dual-method (IQ-TREE3 + MrBayes) phylogeny of the bacterial Hfq family with archaeal SmAP as a structurally motivated outgroup, providing the evolutionary scaffold for the distribution analyses.
2. **Finding 1 (bacteria)** — to test, with a completeness-controlled census across bacterial lifestyles, how Hfq has fared under bacterial genome reduction, and to show that it is lost repeatedly and in two distinct modes; and that the CPR radiation has lost the fold entirely.
3. **Finding 2 (archaea)** — to test, with a completeness-controlled, ab-initio-annotated, structurally-verified census, whether reduced-genome archaea (DPANN, Asgard) retain the fold, and to set the archaeal outcome against the bacterial one.

> **Framing note.** The deep phylogenetic backbone of this superfamily is data-limited — a limitation already reported by Veretnik et al. (2009) and confirmed here — so the phylogeny is used as a scaffold that assigns each sequence to a fold type and domain, not as a resolved deep tree. The novel core is the rigorous, structurally-verified distribution of the fold across the reduced-genome radiations and the domain-level asymmetry it reveals.

---

## 2. Materials and Methods

### 2.1 Superfamily reference set and curation

Sm, Lsm, SmAP and Hfq protein sequences were retrieved from NCBI RefSeq via the E-utilities API. An initial gene-name–based retrieval (6,103 sequences) contained substantial contamination from symbol-similar but unrelated proteins (e.g. "Smaug"/SAM-domain proteins matched by `SmG[Gene Name]`, and eukaryotic "Small Acidic Protein" matched by `SmAP[Gene Name]`). Contaminants were removed with a curated description blacklist and the archaeal Sm set replaced with the manually curated 33 archaeal Sm sequences of Veretnik et al. (2009), yielding a clean reference set of 5,665 sequences.

### 2.2 Bacterial Hfq family dataset

For the focused bacterial Hfq phylogeny, bacterial Hfq sequences were retrieved from RefSeq, clustered at 90% identity with CD-HIT (Li and Godzik 2006; 500 → 293), length-filtered to 50–150 aa (retaining the ~70–110-aa Hfq core; Sobrero and Valverde 2012), aligned with MAFFT (Katoh and Standley 2013), and rooted with five archaeal SmAP outgroup sequences spanning the major archaeal lineages. Unstable ("rogue") taxa were removed with RogueNaRok (Aberer et al. 2013), yielding 225 taxa (220 Hfq + 5 SmAP) and 254 aligned sites.

### 2.3 Structure-guided multiple sequence alignment

Because Sm/Lsm/Hfq proteins are short and highly divergent across domains, plain sequence alignment is unreliable at deep nodes. A structural reference was built from 19 experimentally determined Sm-fold structures spanning all three domains, aligned with FoldMason (Gilchrist et al. 2026) and dereplicated (CD-HIT 95%) into a 25-sequence structural seed, which guided alignment of the full sequence set with MAFFT (`--seed`). After occupancy trimming the analysis alignment comprised 1,101 sequences × 184 columns.

### 2.4 Phylogenetic inference

Maximum-likelihood inference used IQ-TREE3 v3.1.3 (Wong et al. 2026) with ModelFinder (BIC; Kalyaanamoorthy et al. 2017) and ultrafast bootstrap (1,000 replicates; Hoang et al. 2018). Bayesian inference used MrBayes v3.2 (Ronquist et al. 2012) with convergence assessed by the average standard deviation of split frequencies. Topological congruence between ML and Bayesian trees was quantified with DendroPy (Sukumaran and Holder 2010).

### 2.5 Bacterial Hfq-loss census

To test the association between Hfq loss and genome reduction, 71 **complete** bacterial genomes (RefSeq, assembly level "Complete Genome") were sampled across 37 taxa spanning eight lifestyle categories (free-living, facultative/host-associated, spirochete, Actinobacteria, obligate intracellular, mollicute, obligate endosymbiont, and the deep-branching Aquificota). Complete (closed) genomes were used rather than CheckM completeness filtering because highly reduced endosymbionts genuinely lack the universal single-copy markers CheckM relies on; in a closed genome, non-detection is true gene loss rather than an assembly gap. Proteomes were scanned for Hfq with the Pfam PF17209 profile HMM using hmmsearch under the trusted (`--cut_ga`) cutoff (Eddy 2011; Mistry et al. 2021). Hfq presence/absence was related to genome size and lifestyle (point-biserial correlation; per-lifestyle retention rates).

### 2.6 Reduced-genome archaeal and CPR census

Genomes of DPANN, Asgard and CPR/Patescibacteria were retrieved via the NCBI Datasets v2 API (O'Leary et al. 2024), filtered by CheckM completeness ≥ 50% and contamination ≤ 10% (MIMAG medium-quality; Bowers et al. 2017; Parks et al. 2015), with GCA/GCF duplicates removed. Genomes lacking an annotated proteome were predicted ab initio with Prodigal (meta mode; Hyatt et al. 2010). Proteomes were scanned with dual profile HMMs — Sm/Lsm (PF01423) and Hfq (PF17209) — under the trusted cutoff, and each hit typed by its higher-scoring model.

### 2.7 Structural verification

HMM hits from the archaeal census were structurally modelled with ESMFold (Lin et al. 2023; ESM Atlas API) and compared against the experimental Sm-fold anchors with Foldseek (van Kempen et al. 2024); a TM-score ≥ 0.5 to a Sm-fold anchor was taken as structural confirmation. Suspicious tips in the bacterial Hfq tree (the longest branch and removed rogues) were verified the same way.

---

## 3. Results

### 3.1 A curated, contamination-controlled superfamily dataset

Gene-name–based retrieval of 6,103 sequences proved substantially contaminated (~15% of tips were unrelated proteins recruited by symbol-similar names). After curation, 5,665 clean sequences remained; length-filtering and 90% clustering reduced this to 1,107 representatives. Mapping protein type onto the framework tree (Fig. 1), the four expected assemblages — bacterial Hfq (231 tips), archaeal SmAP (27), eukaryotic Lsm (498) and eukaryotic Sm-core (335) — separate into their expected fold-type assemblages, supporting the curation; finer paralogue-level relationships are not resolved at this depth and are not interpreted here (Section 3.2). The bacterial Hfq clade is distinct while the archaeal SmAP sequences fall among the eukaryotic Sm/Lsm assemblages rather than with Hfq, as expected if archaeal Sm is ancestral to the eukaryotic system.

### 3.2 A structure-guided framework and a rooted, dual-method Hfq phylogeny

The structure-guided three-domain tree (1,101 sequences, 184 sites; Q.INSECT+G4) recovers the terminal and mid-depth clades but leaves the deep backbone poorly resolved (only 43% of internal branches reach UFBoot ≥ 95; the bootstrap did not converge). A plain-sequence control alignment gave essentially the same picture (48%, again non-convergent), so structural guidance produced a principled, structurally-calibrated core but did not improve deep-node resolution. This intrinsic limit was already apparent to Veretnik et al. (2009), who reported that including a bacterial outgroup reduced bootstrap support throughout their tree, attributing it to the short, poorly-alignable core shared across domains. We therefore use the tree as a scaffold.

Within bacteria, the focused Hfq family is far better behaved. Over 225 taxa (254 aligned sites, 139 parsimony-informative), the maximum-likelihood and Bayesian trees agree closely where support is high: of 91 ML branches with UFBoot ≥ 95, 86 (94.5%) are recovered in the Bayesian consensus (median PP of matched branches 0.92), and the five archaeal SmAP outgroup sequences form a single bipartition in both trees, permitting consistent rooting (Fig. 2). Disagreement is confined to the poorly-supported deep backbone. The rooted Hfq phylogeny broadly recapitulates bacterial phylum-level taxonomy, with Pseudomonadota (114 tips) and Bacillota (92 tips) each forming largely coherent assemblages (Fig. S1) — the pattern expected under predominantly vertical inheritance. Ten verified tips (the longest branch plus removed rogues) were all confirmed as genuine Hfq folds by ESMFold + Foldseek.

### 3.3 Hfq is repeatedly lost under bacterial genome reduction, in two modes

Across 71 complete bacterial genomes spanning eight lifestyles, Hfq presence tracks genome reduction: Hfq-present genomes have a median size of 4.1 Mb versus 1.2 Mb for Hfq-absent genomes (point-biserial r = 0.34; r = 0.51 with the Actinobacteria excluded, see below). Free-living bacteria almost always encode Hfq (88%), whereas the reduced-genome lifestyles largely lack it: obligate endosymbionts 18%, obligate intracellular 17%, mollicutes 0%, host-associated spirochetes 0% (Fig. 3A). The deep-branching Aquificota, though comparatively small-genomed, retain Hfq (3/3), consistent with the phyletic survey of Sun et al. (2002).

Two distinct modes of loss are evident (Fig. 3B). The first is **reduction-associated**: as coding capacity collapses in endosymbionts (median 0.64 Mb), mollicutes (0.82 Mb) and obligate intracellular bacteria (1.48 Mb), Hfq is preferentially lost — part of the pervasive gene loss that accompanies bacterial genome reduction (Moran & Bennett 2014). The second is **size-independent, lineage-specific**: the Actinobacteria carry no detectable Hfq in any of eight genomes despite large genomes (Mycobacterium 4.4 Mb, Corynebacterium 3.3 Mb, Streptomyces 8.7–9.1 Mb), and the free-living Myxococcus likewise lacks detectable Hfq at 9.1–9.4 Mb. Loss in these lineages cannot be explained by reduction and reflects lineage-specific replacement or divergence of the RNA-chaperone function. (Because absence is defined here at a trusted HMM cutoff, these results indicate the absence of a *detectable canonical* Hfq; a highly divergent homolog below the detection threshold cannot be excluded, consistent with long-standing reports that canonical Hfq is absent from the Actinobacteria.) Loss is also not obligate under reduction: a minority of reduced genomes — including *Wigglesworthia* (0.72 Mb), *Baumannia* and *Francisella* — retain Hfq.

### 3.4 The bacterial CPR/Patescibacteria radiation has lost the fold entirely

Applying the completeness-filtered dual-HMM pipeline to the bacterial reduced-genome radiation CPR/Patescibacteria gave a clean negative: across 397 completeness-passing genomes (290,425 predicted proteins; including 393 Saccharibacteria with otherwise complete ribosomal machinery), no Hfq and no Sm/Lsm protein was detected. That the same pipeline recovered 70 archaeal hits, and that these CPR proteomes carry the expected universal machinery (843 ribosomal-protein annotations), confirm the absence is biological rather than technical. No prior study had examined Hfq or Sm-like proteins in any CPR lineage, so this is the first assessment, and it is a rigorous true absence — the extreme end of the bacterial loss documented in Section 3.3.

### 3.5 DPANN and Asgard archaea retain the Sm fold

In sharp contrast to the bacterial losses, reduced-genome archaea retain the fold. Applying the completeness-filtered dual-HMM pipeline to 50 quality DPANN/Asgard genomes detected Sm/Lsm proteins in all six lineages with sufficient genome quality (Nanoarchaeota, Asgardarchaeota, Lokiarchaeia, Parvarchaeota, Micrarchaeota, Nanohaloarchaeota); all 70 hits typed as Sm/Lsm and none as Hfq. All sampled Lokiarchaeia (Asgard), including the cultured *Promethearchaeum syntrophicum*, retain the fold, as does the DPANN type species *Nanoarchaeum equitans*. This extends to the reduced-genome, MAG-dominated DPANN and Asgard lineages the broad retention of Lsm proteins previously reported across cultured archaea (Payá & Bonete 2023). All 55 hits that yielded confident ESMFold models matched an experimental Sm-fold anchor by Foldseek (TM-score 0.92–1.00; median 0.97), and 49/55 were closest to an archaeal Sm anchor (Fig. 4). That some DPANN/Asgard archaea encode Sm-like proteins was already indicated qualitatively (Reichelt et al. 2018); our contribution is the systematic, completeness-controlled, structurally-verified quantification and its contrast with the bacterial losses.

### 3.6 A domain-level asymmetry in Sm-fold fate under genome reduction

Taken together, the two prokaryotic domains diverge under genome reduction (Fig. 4). In bacteria the Sm fold is repeatedly lost — gradually under genome reduction and abruptly in whole lineages (Actinobacteria) and in the entire CPR radiation. In archaea the same fold is retained across every quality-genome DPANN/Asgard lineage examined, including the most reduced ones. The negative bacterial and CPR results also serve as an internal control: the pipeline reports true absence when the gene is genuinely gone, so the archaeal retention is not an artifact of a method that "finds hits everywhere."

---

## 4. Discussion

- **Central result — a domain-level asymmetry in the fate of a single ancient fold.** Using structure-guided phylogeny and completeness-controlled, structurally-verified censuses, we find that the Sm fold is repeatedly lost across bacteria under genome reduction, yet retained across reduced-genome archaea. The bacterial loss has two modes — reduction-associated (endosymbionts, mollicutes, intracellular; CPR at the extreme) and size-independent lineage loss (Actinobacteria, Myxococcus) — extending the phyletic picture of Sun et al. (2002) to genome scale and showing that Hfq distribution reflects gene loss on multiple axes rather than a single reduction gradient.

- **Why the fates differ.** A functional asymmetry offers a plausible — though census-untested — explanation: the archaeal Sm/SmAP protein is embedded in core RNA metabolism, the *Pyrococcus furiosus* homolog associating broadly with the exosome, ribosome, RNA polymerase and RNA-modification machinery (Reichelt et al. 2023), whereas bacterial Hfq acts mainly as a more peripheral and frequently dispensable small-RNA regulator. Under genome reduction a central, less-redundant RNA-metabolism factor is expected to be retained while a peripheral regulator is preferentially lost.

- **Evolutionary interpretation.** The retained archaeal proteins are Sm/SmAP-type (structurally closest to archaeal anchors), consistent with the eukaryotic Sm/Lsm system deriving from an archaeal ancestor (Collins & Mabbutt 2001; Törő et al. 2001); retention in Asgard (Lokiarchaeia) provides primary data relevant to eukaryogenesis.

- **Novelty and prior work.** That DPANN/Asgard archaea encode Sm-like proteins was already indicated qualitatively (Reichelt et al. 2018); we do not claim first detection. The genuinely new elements are the two-mode bacterial Hfq-loss census, the rigorous CPR absence, the structural verification of the archaeal hits, and the domain-level asymmetry that unifies them.

- **Limitations.** The deep phylogenetic backbone is data-limited and is used as a framework, not a resolved deep tree. Absence is defined at a trusted HMM cutoff, so highly divergent homologs below detection cannot be excluded (relevant to the Actinobacteria and Myxococcus). The bacterial census samples lifestyles rather than exhaustively, and the CPR side rests chiefly on the well-sampled Saccharibacteria, which we treat as the decisive test rather than a domain-wide claim.

---

## 5. Conclusion

A single ancient fold, shared by the RNA-ring proteins of all three domains, meets opposite fates under genome reduction: repeated loss across bacteria — gradual under reduction, wholesale in the Actinobacteria and the CPR radiation — but retention across reduced-genome archaea. Set within an updated, structure-guided phylogeny and verified structurally, this domain-level asymmetry distinguishes genuine gene loss from artifact and points to the differing dispensability of the fold in the two domains, with the archaeal retention bearing on the archaeal ancestry of the eukaryotic Sm/Lsm machinery.

---

## Figures and Tables

| Item | Caption |
|------|---------|
| Fig. 1 | Structure-guided Sm/Lsm/Hfq phylogeny across the three domains, tips coloured by type (Hfq / SmAP / Lsm / Sm-core). |
| Fig. 2 | Rooted, dual-method bacterial Hfq phylogeny (225 taxa): ML/Bayesian support concordance at internal nodes; archaeal SmAP outgroup bold at the base. |
| Fig. 3 | Hfq loss across bacteria. (A) Hfq retention by lifestyle; (B) Hfq presence/absence versus genome size, showing reduction-associated loss and size-independent lineage loss (Actinobacteria, Myxococcus). |
| Fig. 4 | (A) Sm-fold distribution across the reduced-genome radiations: DPANN/Asgard archaea retain, CPR bacteria have lost; (B) structural verification — all 55 archaeal ESMFold hits match a Sm-fold anchor by Foldseek (TM-score ≥ 0.92, median 0.97). |
| Table 1 | Sm/Lsm and Hfq counts per DPANN/Asgard/CPR lineage (genome- and species-level), with completeness. |
| Fig. S1 | The bacterial Hfq phylogeny of Fig. 2 coloured by bacterial phylum (Supplementary). |

## Figure legends

**Figure 1.** Structure-guided Sm/Lsm/Hfq phylogeny across the three domains, tips coloured by protein type (Hfq / SmAP / Lsm / Sm-core). The bacterial Hfq clade is distinct while archaeal SmAP sequences fall among the eukaryotic Sm/Lsm assemblages.

**Figure 2.** Rooted maximum-likelihood phylogeny of the bacterial Hfq family (225 taxa) with ML/Bayesian support concordance mapped at internal nodes (both high / ML only / Bayes only / both weak); the archaeal SmAP outgroup is shown in bold at the base.

**Figure 3.** Hfq loss across bacteria (71 complete genomes, eight lifestyles). (A) Percentage of genomes encoding a detectable Hfq per lifestyle. (B) Hfq presence/absence versus genome size (log scale); reduction-associated loss occurs at small genomes, while the Actinobacteria and Myxococcus lack Hfq at large genome sizes (size-independent lineage loss).

**Figure 4.** (A) Sm-fold distribution across the two prokaryotic reduced-genome radiations: DPANN/Asgard archaea retain Sm/Lsm while CPR bacteria have lost it (0/393 Saccharibacteria etc.). (B) Structural verification: all 55 archaeal ESMFold hits match an experimental Sm-fold anchor by Foldseek (TM-score ≥ 0.92, median 0.97).

**Figure S1 (Supplementary).** The rooted bacterial Hfq phylogeny of Figure 2, coloured by bacterial phylum; Pseudomonadota and Bacillota each form largely coherent assemblages.

**Table 1.** Sm/Lsm and Hfq incidence across the sampled reduced-genome radiations. Genome and species counts are after CheckM completeness filtering (≥50% complete, ≤10% contaminated); "genomes with Sm/Lsm" and "genomes with Hfq" count genomes carrying at least one PF01423 (Sm/Lsm) or PF17209 (Hfq) hit, respectively; "Sm/Lsm hits" and "Hfq hits" are total domain hits summed over genomes; mean completeness is the CheckM mean over each lineage's genomes. Every archaeal lineage retains the Sm fold in nearly all assessable genomes, whereas the bacterial CPR radiation carries neither Sm/Lsm nor Hfq in any of 397 genomes despite comparable assembly completeness — excluding low completeness as an explanation for the bacterial absence.

| Domain (radiation) | Lineage | Genomes | Species | Genomes w/ Sm/Lsm | Genomes w/ Hfq | Sm/Lsm hits | Hfq hits | Mean completeness (%) |
|---|---|--:|--:|--:|--:|--:|--:|--:|
| Archaea (DPANN/Asgard) | *Nanoarchaeota* | 16 | 4 | 14 | 0 | 14 | 0 | 67.9 |
| Archaea (DPANN/Asgard) | *Asgardarchaeota* | 11 | 6 | 10 | 0 | 24 | 0 | 82.9 |
| Archaea (DPANN/Asgard) | *Lokiarchaeia* | 8 | 4 | 8 | 0 | 20 | 0 | 78.5 |
| Archaea (DPANN/Asgard) | *Parvarchaeota* | 7 | 2 | 4 | 0 | 4 | 0 | 66.9 |
| Archaea (DPANN/Asgard) | *Micrarchaeota* | 4 | 4 | 4 | 0 | 4 | 0 | 86.2 |
| Archaea (DPANN/Asgard) | *Nanohaloarchaeota* | 4 | 3 | 4 | 0 | 4 | 0 | 85.4 |
| **Archaea — subtotal** | | **50** | **23** | **44** | **0** | **70** | **0** | **75.6** |
| Bacteria (CPR/Patescibacteria) | *Saccharibacteria* | 393 | 15 | 0 | 0 | 0 | 0 | 82.0 |
| Bacteria (CPR/Patescibacteria) | *Candidatus* Absconditabacteria | 3 | 3 | 0 | 0 | 0 | 0 | 81.5 |
| Bacteria (CPR/Patescibacteria) | *Patescibacteria* (unclassified) | 1 | 1 | 0 | 0 | 0 | 0 | 80.7 |
| **Bacteria — subtotal** | | **397** | **19** | **0** | **0** | **0** | **0** | **82.0** |

---

## Data Availability

All analysis code and derived data are available in the project repository (https://github.com/Carlo-Broschi/bio-c_sm-fold-genome-reduction) and archived at Zenodo (doi:10.5281/zenodo.21202213). Protein and genome accessions are listed in the supplementary material; predicted structures are regenerable from accessions via the provided scripts. The two companion analyses that this study consolidates are archived separately (bio-a Hfq: 10.5281/zenodo.21197822; bio-b Sm/Lsm: 10.5281/zenodo.21197824).

---

## References

<!-- 最終リストは REFERENCES_gbe_final.md（26件）。投稿時に本文引用と最終照合。 -->

See `REFERENCES_gbe_final.md` (26 entries, GBE author–date, DOI-verified).
