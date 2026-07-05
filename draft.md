# The fate of the Sm fold under genome reduction: a structure-informed phylogeny across the three domains of life — Manuscript Draft

**Project:** bio-c — integrated Sm/Lsm/Hfq study
**Author:** Minoru Nakai
**Target journal:** Genome Biology and Evolution / Molecular Biology and Evolution
**Status:** Draft assembly (2026-07); integrates the QC-locked bio-a (Hfq) and bio-b (Sm/Lsm) analyses plus a new bacterial Hfq-loss census.

---

## Abstract

The Sm/Lsm/Hfq superfamily builds the RNA-associated toroidal rings that underlie processes from eukaryotic pre-mRNA splicing to bacterial small-RNA regulation, and its distribution across the three domains bears on the archaeal ancestry of the eukaryotic spliceosome. Building a structure-guided three-domain phylogeny of the superfamily and a rooted, dual-method (maximum-likelihood and Bayesian) phylogeny of the bacterial Hfq family, we ask how the Sm fold has fared under genome reduction in each domain. In bacteria, a completeness-controlled census of Hfq across 71 complete genomes spanning eight lifestyles shows that Hfq loss tracks genome reduction (Hfq-present genomes median 4.1 Mb versus 1.2 Mb for Hfq-absent) but follows two distinct modes: reduction-associated loss in endosymbionts, mollicutes and obligate intracellular bacteria, and size-independent lineage loss in the Actinobacteria (3–9 Mb genomes, none with detectable Hfq) and Myxococcus. The bacterial CPR/Patescibacteria radiation has lost the fold entirely (0/397 quality genomes). In sharp contrast, reduced-genome archaea (DPANN, Asgard) retain the Sm fold in every quality-genome lineage examined, with all 55 confidently modelled hits matching an experimental Sm-fold anchor (TM-score ≥ 0.91). The Sm fold thus shows a domain-level asymmetry in its fate under genome reduction — repeatedly lost across bacteria yet retained across reduced-genome archaea — a contrast we draw rigorously and interpret in terms of the differing functional dispensability of the fold in the two domains.

---

## Significance statement

The Sm/Lsm/Hfq fold builds RNA-associated rings found across all cellular life, and its fate in reduced-genome lineages informs the archaeal origin of the eukaryotic spliceosome. Using a structure-guided phylogeny and completeness-controlled, structurally-verified censuses, we show that the fold is repeatedly lost across bacteria under genome reduction — and, independently, in whole lineages such as the Actinobacteria — yet is retained across reduced-genome archaea (DPANN, Asgard). This domain-level asymmetry, drawn rigorously here, separates genuine gene loss from detection and assembly artifacts and points to a functional-dispensability basis for the divergent fates of a single ancient fold.

---

## 1. Introduction

### Background

The Sm/Lsm protein family is one of the most ancient and conserved families in the history of life. In eukaryotes, seven Sm proteins (SmB, SmD1, SmD2, SmD3, SmE, SmF, SmG) and eight Lsm proteins (Lsm1–Lsm8) form heptameric rings that associate with snRNAs to constitute the spliceosome and mRNA-decay machinery. Archaeal homologs (Sm-like archaeal proteins, SmAP) form similar homomeric rings involved in RNA binding, and the bacterial counterpart Hfq shares the same Sm fold — an N-terminal α-helix over a strongly bent five-stranded antiparallel β-sheet (Sm1 motif, β1–β3; Sm2 motif, β4–β5) — despite low sequence identity, assembling into a homohexameric ring rather than a heptamer. Across these forms the fold performs closely related RNA-associated functions: the eukaryotic Sm/Lsm rings scaffold the spliceosomal snRNPs and the mRNA-decay machinery, archaeal SmAP proteins bind uridine-rich RNA, and bacterial Hfq acts as a global RNA chaperone that mediates small-RNA–mRNA pairing in post-transcriptional regulation (Vogel and Luisi 2011). The high-resolution structures of representatives from all three domains established the shared toroidal architecture and the uridine-binding pockets that define the family (Collins & Mabbutt 2001; Törő et al. 2001). Their evolutionary relationships across the three domains therefore bear both on the early evolution of the spliceosome (Veretnik et al. 2009) and on eukaryogenesis, since the eukaryotic Sm/Lsm machinery is thought to derive from an archaeal ancestor.

### Gap

The most comprehensive phylogenetic study of the Sm/Lsm family to date (Veretnik et al. 2009) analysed 335 sequences from 80 species using ClustalW alignment and PhyML. In the intervening ~17 years, sequence data have grown by more than an order of magnitude, phylogenetic methods have advanced (structure-guided alignment, ModelFinder, ultrafast bootstrap, Bayesian inference with convergence diagnostics), and — critically — the reduced-genome radiations that dominate the two prokaryotic domains have become sampled. On the archaeal side these are the ultra-small-celled **DPANN** superphylum, delimited from single-cell genomics of "microbial dark matter" and typified by reduced genomes and frequent episymbiosis (Rinke et al. 2013), and the **Asgard** archaea, the closest known archaeal relatives of eukaryotes and hence central to eukaryogenesis (Spang et al. 2015; Zaremba-Niedzwiedzka et al. 2017), now represented by the cultured Lokiarchaeon *Promethearchaeum syntrophicum* (Imachi et al. 2020). On the bacterial side, the **Candidate Phyla Radiation (CPR/Patescibacteria)** comprises well over 15% of bacterial diversity, again with ultra-small cells, streamlined genomes and an episymbiotic lifestyle (Brown et al. 2015; Castelle and Banfield 2018). All three radiations are shaped by the reductive genome evolution that also drives obligate endosymbionts and intracellular pathogens (McCutcheon and Moran 2011; Moran & Bennett 2014). Whether these deeply-branching, reduced-genome lineages retain the Sm fold — and whether its fate differs between the bacterial and archaeal radiations — has not been examined with modern, completeness-controlled, structurally-verified methods. The obstacles are methodological: low-sensitivity searches confound true loss with failure to detect divergent sequences, and metagenome-assembled genomes (MAGs) confound absence with incomplete assembly and annotation.

### Aims

This study is organised as a phylogenetic *framework* plus two comparative-distribution *findings*.

1. **Framework** — to place the Sm/Lsm/Hfq superfamily in an updated, structure-guided three-domain phylogeny, and to reconstruct a rooted, dual-method (IQ-TREE3 + MrBayes) phylogeny of the bacterial Hfq family with archaeal SmAP as a structurally motivated outgroup, providing the evolutionary scaffold for the distribution analyses.
2. **Finding 1 (bacteria)** — to test, with a completeness-controlled census across bacterial lifestyles, how Hfq has fared under bacterial genome reduction, and to show that it is lost repeatedly and in two distinct modes; and that the CPR radiation has lost the fold entirely.
3. **Finding 2 (archaea)** — to test, with a completeness-controlled, ab-initio-annotated, structurally-verified census, whether reduced-genome archaea (DPANN, Asgard) retain the fold, and to set the archaeal outcome against the bacterial one.

> **Framing note.** The deep phylogenetic backbone of this superfamily is data-limited — a limitation already reported by Veretnik et al. (2009) and confirmed here — so the phylogeny is used as a scaffold that assigns each sequence to a fold type and domain, not as a resolved deep tree. The novel core is the rigorous, structurally-verified distribution of the fold across the reduced-genome radiations and the domain-level asymmetry it reveals.

---

## 2. Materials and Methods

### 2.1 Superfamily reference set and curation

Sm, Lsm, SmAP and Hfq protein sequences were retrieved from NCBI RefSeq (accessed June–July 2026) through the E-utilities API (`esearch`/`efetch`), querying the eukaryotic Sm paralogues (SmB, SmD1, SmD2, SmD3, SmE, SmF, SmG), the eukaryotic Lsm paralogues (Lsm1–Lsm8), archaeal Sm-like proteins, and bacterial Hfq (up to 500 sequences per query). An initial gene-name–based retrieval (6,103 sequences) contained substantial contamination from symbol-similar but unrelated proteins: for example, `SmG[Gene Name]` recruited hundreds of "Smaug"/SAM-domain proteins, and `SmAP[Gene Name]` returned eukaryotic "Small Acidic Protein" entries and no genuine archaeal Sm. Contaminants were removed with a curated description blacklist applied to the FASTA headers, and the archaeal Sm set was replaced with the manually curated 33 archaeal Sm sequences of Veretnik et al. (2009), yielding a clean reference set of 5,665 sequences. All retrieval and filtering scripts are in the project repository (Data Availability).

### 2.2 Bacterial Hfq family dataset

For the focused bacterial Hfq phylogeny, bacterial Hfq sequences were retrieved from RefSeq with the query `hfq[Gene Name] AND bacteria[Organism] AND refseq[filter]` (19,778 hits; the top 500 downloaded). Sequences were clustered at 90% amino-acid identity with CD-HIT v4.8.1 (Li and Godzik 2006; `-c 0.9 -n 5`), reducing 500 to 293 representatives, then length-filtered to 50–150 aa (retaining the ~70–110-aa Hfq core while removing fragments and fusion proteins; Sobrero and Valverde 2012), leaving 229 sequences. These were aligned with MAFFT v7 (Katoh and Standley 2013; `--auto`) and rooted with five archaeal SmAP outgroup sequences spanning the major archaeal lineages (*Archaeoglobus fulgidus* NP_069198.1 and *Methanothermobacter thermautotrophicus* O26745, Euryarchaeota; *Pyrobaculum aerophilum* AAL63028.1 and *Sulfolobus solfataricus* NP_341755.1, Crenarchaeota; *Nanoarchaeum equitans* NP_963332.1, Nanoarchaeota). Unstable ("rogue") taxa were identified from the Bayesian posterior tree set with RogueNaRok (Aberer et al. 2013; compiled from source) and the nine taxa exceeding a raw-improvement score of 0.5 were removed, giving a final alignment of 225 taxa (220 Hfq + 5 SmAP) and 254 aligned sites (139 parsimony-informative).

### 2.3 Structure-guided multiple sequence alignment

Because Sm/Lsm/Hfq proteins are short and highly divergent across domains, plain sequence alignment is unreliable at deep nodes (a straightforward MAFFT alignment expanded to ~92% gaps). A structural reference was therefore built from 19 experimentally determined Sm-fold structures spanning all three domains (eukaryotic Sm/U1 snRNP, archaeal SmAP, bacterial Hfq; PDB accessions in Supplementary Table S1). These were structurally aligned with FoldMason (Gilchrist et al. 2026; `easy-msa`, run locally) and dereplicated at 95% identity with CD-HIT into a 25-sequence structural seed spanning the three domains. The seed was used to guide alignment of the redundancy-reduced (CD-HIT 90%; 1,107 representatives) superfamily sequence set with MAFFT (`--seed`); after occupancy trimming (removing columns present in <10% of sequences) the analysis alignment comprised 1,101 sequences × 184 columns, with a structurally-defined core of ~76 columns corresponding to the Sm fold.

### 2.4 Phylogenetic inference

Maximum-likelihood inference used IQ-TREE3 v3.1.3 (Wong et al. 2026; `-m TEST -B 1000 -T AUTO`) with the best-fit model chosen by ModelFinder under the Bayesian Information Criterion (Kalyaanamoorthy et al. 2017) — Q.INSECT+I+G4 for the bacterial Hfq alignment and Q.INSECT+G4 for the structure-guided superfamily alignment — and node support from 1,000 ultrafast bootstrap replicates (Hoang et al. 2018), with UFBoot ≥ 95 taken as strong support. Bayesian inference used MrBayes v3.2 (Ronquist et al. 2012) with the amino-acid model fixed to VT+G4 (`prset aamodelpr=fixed(vt)`; chosen because the default mixed-model sampling did not converge), two independent runs of four chains, 25% relative burn-in, and convergence judged by the average standard deviation of split frequencies (ASDSF); the bacterial Hfq analysis reached ASDSF 0.047. Topological congruence between the ML and Bayesian trees was quantified with DendroPy v5.0.8 (Sukumaran and Holder 2010) by comparing bipartitions on the shared taxon set (namespace-independent, to accommodate label sanitisation differences).

### 2.5 Bacterial Hfq-loss census

To test the association between Hfq loss and genome reduction, 71 **complete** bacterial genomes (RefSeq, assembly level "Complete Genome") were sampled across 37 taxa spanning eight lifestyle categories (free-living, facultative/host-associated, host-associated spirochete, Actinobacteria, obligate intracellular, mollicute, obligate endosymbiont, and the deep-branching Aquificota; the full taxon–lifestyle table is in the repository). This is a stratified sample designed to span the genome-reduction gradient rather than an unbiased survey of bacterial diversity. Complete (closed) genomes were required rather than CheckM completeness filtering, because highly reduced endosymbionts genuinely lack the universal single-copy markers CheckM relies on and would be spuriously discarded; in a closed genome, non-detection is true gene loss rather than an assembly gap. Genomes and their annotated proteomes were retrieved through the NCBI Datasets v2 API (O'Leary et al. 2024) with genome size recorded per assembly. Proteomes were scanned for Hfq with the Pfam profile HMM PF17209 (Mistry et al. 2021) using `hmmsearch` (HMMER v3.4; Eddy 2011) under the trusted gathering cutoff (`--cut_ga`); a genome was scored Hfq-present if it carried ≥1 hit. Presence/absence was related to genome size by the point-biserial correlation, computed both per genome and per taxon (taxon-median genome size, majority call) to confirm robustness to sampling multiple genomes per taxon, and summarised as per-lifestyle retention rates.

### 2.6 Reduced-genome archaeal and CPR census

Genomes of DPANN (nine lineages) and Asgard (five classes) archaea and of the bacterial CPR/Patescibacteria were retrieved through the NCBI Datasets v2 API (O'Leary et al. 2024) and filtered by CheckM completeness ≥ 50% and contamination ≤ 10% (the MIMAG medium-quality threshold; Bowers et al. 2017; Parks et al. 2015), with GCA/GCF duplicate assemblies collapsed to one record (RefSeq preferred). Genomes lacking an annotated proteome — common among metagenome-assembled genomes — were gene-called ab initio with Prodigal in metagenomic mode (Hyatt et al. 2010), removing annotation-gap artefacts. Proteomes were scanned with two Pfam profile HMMs, Sm/Lsm (PF01423) and Hfq (PF17209), with `hmmsearch --cut_ga`; each hit was typed as Sm/Lsm or Hfq by its higher-scoring model. Because presence is far more robust to genome incompleteness than absence, hit counts were aggregated at genome, species and lineage level, and lineages with no completeness-passing genome were reported as data-insufficient rather than as absences.

### 2.7 Structural verification

To confirm that the archaeal HMM hits represent genuine Sm folds rather than sequence-level chance matches, each hit was structurally modelled with ESMFold via the ESM Atlas API (Lin et al. 2023), and models with mean pLDDT ≥ 0.7 were compared against the 19 experimental Sm-fold anchors with Foldseek v10 (`easy-search`, TM-align mode; van Kempen et al. 2024). A TM-score ≥ 0.5 to an Sm-fold anchor — the conventional same-fold threshold — was taken as structural confirmation, and the best-matching anchor recorded for each hit. Suspicious tips in the bacterial Hfq tree (the single longest branch and the removed rogue taxa) were verified the same way against experimental Hfq structures.

---

## 3. Results

### 3.1 A curated, contamination-controlled superfamily dataset

Gene-name–based retrieval of 6,103 sequences proved substantially contaminated (~15% of tips were unrelated proteins recruited by symbol-similar names). After curation, 5,665 clean sequences remained; length-filtering and 90% clustering reduced this to 1,107 representatives. Mapping protein type onto the framework tree (Fig. 1), the four expected assemblages — bacterial Hfq (231 tips), archaeal SmAP (27), eukaryotic Lsm (498) and eukaryotic Sm-core (335) — separate into their expected fold-type assemblages, supporting the curation; finer paralogue-level relationships are not resolved at this depth and are not interpreted here (Section 3.2). The bacterial Hfq clade is distinct while the archaeal SmAP sequences fall among the eukaryotic Sm/Lsm assemblages rather than with Hfq, as expected if archaeal Sm is ancestral to the eukaryotic system.

### 3.2 A structure-guided framework and a rooted, dual-method Hfq phylogeny

The structure-guided three-domain tree (1,101 sequences, 184 sites; Q.INSECT+G4) recovers the terminal and mid-depth clades but leaves the deep backbone poorly resolved (only 43% of internal branches reach UFBoot ≥ 95; the bootstrap did not converge). A plain-sequence control alignment gave essentially the same picture (48%, again non-convergent), so structural guidance produced a principled, structurally-calibrated core but did not improve deep-node resolution. This intrinsic limit was already apparent to Veretnik et al. (2009), who reported that including a bacterial outgroup reduced bootstrap support throughout their tree, attributing it to the short, poorly-alignable core shared across domains. We therefore use the tree as a scaffold.

Within bacteria, the focused Hfq family is far better behaved. Over 225 taxa (254 aligned sites, 139 parsimony-informative), the maximum-likelihood and Bayesian trees agree closely where support is high: of 91 ML branches with UFBoot ≥ 95, 86 (94.5%) are recovered in the Bayesian consensus (median PP of matched branches 0.92), and the five archaeal SmAP outgroup sequences form a single bipartition in both trees, permitting consistent rooting (Fig. 2). Disagreement is confined to the poorly-supported deep backbone. The rooted Hfq phylogeny broadly recapitulates bacterial phylum-level taxonomy, with Pseudomonadota (114 tips) and Bacillota (92 tips) each forming largely coherent assemblages (Fig. S1) — the pattern expected under predominantly vertical inheritance. Ten verified tips (the longest branch plus removed rogues) were all confirmed as genuine Hfq folds by ESMFold + Foldseek.

### 3.3 Hfq is repeatedly lost under bacterial genome reduction, in two modes

We sampled 71 complete bacterial genomes across 37 taxa chosen to span eight lifestyle categories from free-living to obligate endosymbiont; this is a stratified, illustrative sample designed to cover the reduction gradient rather than an unbiased survey of bacterial diversity, so the per-lifestyle rates below are illustrative and the size–presence relationship is the robust quantitative result. Hfq presence tracks genome reduction: Hfq-present genomes have a median size of 4.1 Mb versus 1.2 Mb for Hfq-absent genomes (point-biserial r = 0.34; r = 0.51 with the Actinobacteria excluded, see below). Collapsing to one value per taxon (taxon-median genome size, majority Hfq call) leaves the association essentially unchanged (r = 0.34; 0.51 excluding Actinobacteria), so it is not an artifact of sampling multiple genomes per taxon. Free-living bacteria almost always encode Hfq (88%), whereas the reduced-genome lifestyles largely lack it: obligate endosymbionts 18%, obligate intracellular 0%, mollicutes 0%, host-associated spirochetes 0% (Fig. 3A). The deep-branching Aquificota, though comparatively small-genomed, retain Hfq (3/3), consistent with the phyletic survey of Sun et al. (2002).

Two distinct modes of loss are evident (Fig. 3B). The first is **reduction-associated**: as coding capacity collapses in endosymbionts (median 0.64 Mb), mollicutes (0.82 Mb) and obligate intracellular bacteria (1.18 Mb; all 10 lacking Hfq), Hfq is preferentially lost — part of the pervasive gene loss that accompanies bacterial genome reduction (Moran & Bennett 2014; McCutcheon et al. 2024). The second is **size-independent, lineage-specific**: the Actinobacteria — included here specifically to test whether loss can be decoupled from genome size — carry no detectable Hfq in any of eight genomes despite large genomes (Mycobacterium 4.4 Mb, Corynebacterium 3.3 Mb, Streptomyces 8.7–9.1 Mb), and the free-living Myxococcus likewise lacks detectable Hfq at 9.1–9.4 Mb. Loss in these lineages cannot be explained by reduction and reflects lineage-specific replacement or divergence of the RNA-chaperone function. (Because absence is defined here at a trusted HMM cutoff, these results indicate the absence of a *detectable canonical* Hfq; a highly divergent homolog below the detection threshold cannot be excluded, consistent with long-standing reports that canonical Hfq is absent from the Actinobacteria.) Loss is also not obligate under reduction: a minority of reduced-genome endosymbionts — including *Wigglesworthia* (0.72 Mb) and *Baumannia* — retain Hfq.

### 3.4 The bacterial CPR/Patescibacteria radiation has lost the fold entirely

Applying the completeness-filtered dual-HMM pipeline to the bacterial reduced-genome radiation CPR/Patescibacteria gave a clean negative: across 397 completeness-passing genomes (290,425 predicted proteins; including 393 Saccharibacteria with otherwise complete ribosomal machinery), no Hfq and no Sm/Lsm protein was detected. That the same pipeline recovered 70 archaeal hits, and that these CPR proteomes carry the expected universal machinery (843 ribosomal-protein annotations), confirm the absence is biological rather than technical. No prior study had examined Hfq or Sm-like proteins in any CPR lineage, and recent surveys of CPR biology do not address them (Srinivas et al. 2024), so this is the first such assessment and a rigorous true absence — the extreme end of the bacterial loss documented in Section 3.3.

### 3.5 DPANN and Asgard archaea retain the Sm fold

In sharp contrast to the bacterial losses, reduced-genome archaea retain the fold. Applying the completeness-filtered dual-HMM pipeline to 50 quality DPANN/Asgard genomes detected Sm/Lsm proteins in all six lineages with sufficient genome quality (Nanoarchaeota, Asgardarchaeota, Lokiarchaeia, Parvarchaeota, Micrarchaeota, Nanohaloarchaeota); all 70 hits typed as Sm/Lsm and none as Hfq. All sampled Lokiarchaeia (Asgard), including the cultured *Promethearchaeum syntrophicum*, retain the fold, as does the DPANN type species *Nanoarchaeum equitans*. This extends to the reduced-genome, MAG-dominated DPANN and Asgard lineages the broad retention of Lsm proteins previously reported across cultured archaea (Payá & Bonete 2023), where these proteins have increasingly documented regulatory roles (Payá et al. 2024; Li et al. 2025). All 55 hits that yielded confident ESMFold models matched an experimental Sm-fold anchor by Foldseek (TM-score ≥ 0.91; median 0.97), and 49/55 were closest to an archaeal Sm anchor (Fig. 4); a representative superposition of an ESMFold model on its experimental anchor is shown in Figure 5. That some DPANN/Asgard archaea encode Sm-like proteins was already indicated qualitatively (Reichelt et al. 2018); our contribution is the systematic, completeness-controlled, structurally-verified quantification and its contrast with the bacterial losses.

### 3.6 A domain-level asymmetry in Sm-fold fate under genome reduction

Taken together, the two prokaryotic domains diverge under genome reduction (Fig. 4). In bacteria the Sm fold is repeatedly lost — gradually under genome reduction and abruptly in whole lineages (Actinobacteria) and in the entire CPR radiation. In archaea the same fold is retained across every quality-genome DPANN/Asgard lineage examined, including the most reduced ones. The negative bacterial and CPR results also serve as an internal control: the pipeline reports true absence when the gene is genuinely gone, so the archaeal retention is not an artifact of a method that "finds hits everywhere."

---

## 4. Discussion

- **Central result — a domain-level asymmetry in the fate of a single ancient fold.** Using structure-guided phylogeny and completeness-controlled, structurally-verified censuses, we find that the Sm fold is repeatedly lost across bacteria under genome reduction, yet retained across reduced-genome archaea. The bacterial loss has two modes — reduction-associated (endosymbionts, mollicutes, intracellular; CPR at the extreme) and size-independent lineage loss (Actinobacteria, Myxococcus) — extending the phyletic picture of Sun et al. (2002) to genome scale and showing that Hfq distribution reflects gene loss on multiple axes rather than a single reduction gradient.

- **Why the fates differ.** A functional asymmetry offers a plausible — though census-untested — explanation: the archaeal Sm/SmAP protein is embedded in core RNA metabolism, the *Pyrococcus furiosus* homolog associating broadly with the exosome, ribosome, RNA polymerase and RNA-modification machinery (Reichelt et al. 2023), whereas bacterial Hfq — though a central post-transcriptional regulator in the bacteria that retain it — is a more specialized factor that is evidently dispensable in many lineages, as its repeated loss documented here shows. Under genome reduction a core, less-redundant RNA-metabolism factor is expected to be retained while a more dispensable, specialized regulator is preferentially lost.

- **Evolutionary interpretation.** The retained archaeal proteins are Sm/SmAP-type (structurally closest to archaeal anchors), consistent with the eukaryotic Sm/Lsm system deriving from an archaeal ancestor (Collins & Mabbutt 2001; Törő et al. 2001); retention in Asgard (Lokiarchaeia) provides primary data relevant to eukaryogenesis. The value of structure-based homology detection for this fold is underscored by its recurrence even beyond cellular life — recent work identifies LSm-like folds in bacteriophage proteins (Kim et al. 2025).

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
| Fig. 4 | (A) Sm-fold distribution across the reduced-genome radiations: DPANN/Asgard archaea retain, CPR bacteria have lost; (B) structural verification — all 55 archaeal ESMFold hits match a Sm-fold anchor by Foldseek (TM-score ≥ 0.91, median 0.97). |
| Fig. 5 | Structural verification example: an archaeal ESMFold model superposed on its experimental Sm-fold anchor. |
| Table 1 | Sm/Lsm and Hfq counts per DPANN/Asgard/CPR lineage (genome- and species-level), with completeness. |
| Fig. S1 | The bacterial Hfq phylogeny of Fig. 2 coloured by bacterial phylum (Supplementary). |

## Figure legends

**Figure 1.** Structure-guided Sm/Lsm/Hfq phylogeny of the superfamily (1,101 sequences), shown as an unrooted fan with tips coloured by protein type in a colour-blind-safe palette (Hfq, vermillion; Lsm, blue; Sm-core, orange; archaeal SmAP, purple; unclassified, grey). The bacterial Hfq clade is distinct while archaeal SmAP sequences fall among the eukaryotic Sm/Lsm assemblages.

**Figure 2.** Rooted maximum-likelihood phylogeny of the bacterial Hfq family (225 taxa). Internal-node dots show the concordance of node support between the ML and Bayesian analyses (both high / ML only / Bayes only / both weak), in a colour-blind-safe palette. For legibility only the five archaeal SmAP outgroup taxa are labelled (in bold, at the base, defining the root); the full phylum-annotated tree with all tip labels is Supplementary Figure S1.

**Figure 3.** Hfq loss across bacteria (71 complete genomes, eight lifestyles). (A) Percentage of genomes encoding a detectable Hfq per lifestyle. (B) Hfq presence/absence versus genome size (log scale); reduction-associated loss occurs at small genomes, while the Actinobacteria and Myxococcus lack Hfq at large genome sizes (size-independent lineage loss).

**Figure 4.** (A) Sm-fold distribution across the two prokaryotic reduced-genome radiations: DPANN/Asgard archaea retain Sm/Lsm while CPR bacteria have lost it (0/393 Saccharibacteria etc.). (B) Structural verification: all 55 archaeal ESMFold hits match an experimental Sm-fold anchor by Foldseek (TM-score ≥ 0.91, median 0.97).

**Figure 5.** Structural verification of an archaeal Sm/Lsm hit. The ESMFold model of a representative DPANN/Asgard hit (rainbow, N→C terminus) is superposed on its best-matching experimental Sm-fold anchor (PDB 1I4K; grey), showing the canonical Sm fold — an N-terminal α-helix over a bent five-stranded antiparallel β-sheet (Foldseek TM-score 0.97). All 55 confidently modelled hits matched an experimental Sm-fold anchor in this way (Fig. 4B).

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

## Declarations

### Use of AI tools

During this study the author used Anthropic's Claude — accessed through the Claude Code command-line interface (models in the Claude Opus 4 family) — as an assistive tool. Claude was used to help with: retrieval and parsing of protein and genome data from NCBI; writing and running the analysis pipelines (sequence curation, structure-guided alignment, maximum-likelihood and Bayesian phylogenetic inference, profile-HMM presence/absence censuses, and ESMFold/Foldseek structural verification); statistical analysis; generation of the figures; drafting and editing of the manuscript text; and compilation and formatting of the reference list. All study-design decisions, scientific interpretations, and conclusions were made by the author, who reviewed and verified the analyses and their outputs and takes full responsibility for the entire content of the manuscript, including any parts produced with AI assistance. To enable independent verification, all analysis code is publicly available (see Data Availability). In line with COPE guidance, AI tools are not listed as authors.

### Competing interests

The author declares no competing interests.

---

## References

<!-- 最終リストは REFERENCES_gbe_final.md（26件）。投稿時に本文引用と最終照合。 -->

See `REFERENCES_gbe_final.md` (26 entries, GBE author–date, DOI-verified).
