# bio-c format & figure benchmarking — advisory report

**Manuscript:** *The fate of the Sm fold under genome reduction: a structure-informed phylogeny across the three domains of life* (bio-c), targeted at *Genome Biology and Evolution* (GBE) as an **Article**.

**Scope of this report:** format and figure **advisory only**. Nothing here rewrites the manuscript, re-derives any number, or changes any scientific claim — the science is treated as final. All comparators are recent GBE Articles cited by DOI for verification.

---

## Executive summary

bio-c was benchmarked against **11 recent GBE Articles (2019–2024)** chosen to match it in *kind* — protein-family phylogenetics, gene gain/loss and presence-absence censuses across genomes, structure-informed molecular evolution, and reduced-genome / endosymbiont gene loss. Three headline findings:

1. **Display items: adequately provisioned, lean side of normal.** bio-c has 4 main figures + 1 table = **5 display items** (+1 supplementary figure) vs a comparator median of **7** (range 3–9). This is within range (matched by the lower end of the peer set), and the display *types* are the right ones — trees and quantitative census plots dominate the field and bio-c leads with both. Not under-provisioned, not over-provisioned. There is headroom under GBE's ≤8-item limit to add **one structural-render panel**, which would be worthwhile given the "structure-informed" framing (see §2/§3).

2. **References: a clear outlier — markedly under-referenced.** bio-c cites **26** works; the comparators cite **62–126 (median 79)**. bio-c sits *below the minimum of the entire peer set*. For a study spanning three domains of life, two protein superfamilies, phylogenetics, structural bioinformatics and genome reduction, 26 references is low for a GBE Article. This is the single most conspicuous format gap. *(Reference count only — I am not asserting any specific citation is missing; the literature breadth is simply thin relative to peers.)*

3. **Figures: two production tiers.** The two census figures (**Fig 3, Fig 4**) are publication-quality. The trees are weaker: **Fig 2** (the 225-taxon Hfq tree rendered on a 10 × 26-inch canvas) is **below par as a main figure** — at journal column width its 225 tip labels become an illegible fringe — and is the highest-value figure fix in the paper. **Fig 1** (the 1,097-tip fan) is acceptable but needs a colour-blind-safe recolour, a tighter crop, and removal of its embedded title. **Fig S1** is acceptable as a supplementary item.

![bio-c vs comparator distribution]({{artifact:art_d55b6133-4758-4f8d-ab89-69527331219e}})

*bio-c (red star) against the 11 comparators (grey) on main figures, display items, and references. Display items and figures are slightly below median but within range; references fall below the entire comparator distribution.*

---

# Benchmark: bio-c vs comparable recent GBE Articles

*11 GBE Articles (2019–2024), matched to bio-c in KIND: protein-family phylogenetics, gene gain/loss & presence/absence censuses across genomes, structure-informed molecular evolution, and reduced-genome/endosymbiont gene-loss studies. See the annotated list at the end for DOIs.*

| Study (first author, kind) | Year | Main figs | Tables | Display items | Fig types (main) | Multipanel | Refs | Body words\* |
|---|--:|--:|--:|--:|---|--:|--:|--:|
| **bio-c (this study)** — structure-informed protein-family phylogeny + reduced-genome gene-loss census | 2026 | **4** | **1** | **5** (+1 supp fig) | tree×3 (2 main + 1 supp), quant×2 (each 2-panel: bar+scatter, bar+histogram) | 2 of 4 | **26** | ~2,437 |
| Saito et al. 2019 — cross-domain protein-family molecular evolution (+structure) | 2019 | 5 | 2 | 7 | structure×3, tree×2, quant×1 | 3 of 5 | 65 | ~8,185 |
| Brueckner et al. 2020 — cross-domain gene-content census | 2020 | 5 | 1 | 6 | quant×3, tree×1, schematic×1 | 2 of 5 | 65 | ~6,430 |
| Belato et al. 2020 — protein-family phylogeny | 2020 | 3 | 1 | 4 | tree×3 | 0 of 3 | 100 | ~7,478 |
| Aidlin Harari et al. 2020 — protein-family molecular evolution (+structure) | 2020 | 6 | 1 | 7 | tree×3, structure×3, selection×2, synteny×1 | 1 of 6 | 126 | ~11,010 |
| Boohar et al. 2023 — structure-informed protein-family phylogeny + distribution | 2023 | 6 | 0 | 6 | structure×4, tree×1, quant×1 | 5 of 6 | 80 | ~8,139 |
| Gondhalekar et al. 2023 — cross-domain functional-category census | 2023 | 6 | 2 | 8 | quant×6 | 2 of 6 | 76 | ~10,352 |
| Sinha et al. 2023 — convergent gene-loss across lineages | 2023 | 6 | 2 | 8 | quant×3, tree×2, synteny×1, selection×1 | 0 of 6 | 106 | ~11,749 |
| Ward et al. 2024 — reduced-genome gene-loss (endosymbiont) | 2024 | 5 | 0 | 5 | quant×2, tree×2, synteny×1, selection×1 | 2 of 5 | 97 | ~10,016 |
| Odelgard et al. 2024 — protein-family phylogeny + expansion census | 2024 | 8 | 0 | 8 | quant×7, tree×3, structure×1 | 8 of 8 | 62 | ~9,494 |
| Irisarri et al. 2024 — protein-family phylogeny + distribution | 2024 | 3 | 0 | 3 | tree×2, structure×1 | 2 of 3 | 65 | ~6,980 |
| Luiselli et al. 2024 — genome-reduction simulation | 2024 | 7 | 2 | 9 | quant×6, schematic×1 | 7 of 7 | 79 | ~8,596 |
| **Comparator median (n=11)** | — | **6** | **1** | **7** | — | — | **79** | ~8,600 |

\* **Body words**: for comparators, the full text from Introduction through the end of Materials & Methods (GBE prints Methods last), so it includes Methods and all in-text material before the reference list. bio-c's **~2,437** is the same window — Introduction→Conclusion **including** its Methods section (Methods alone is only ~540 words). Measured identically, bio-c's body is roughly a **quarter** of the comparator median (~8,600) and below the comparator minimum (~6,400). Figure counts are numbered main-text figures; **display items = main figures + main tables** (supplementary items excluded). Reference counts: OpenAlex `referenced_works_count` for comparators, and the 26-entry formatted list for bio-c. Figure types classified from each paper's figure mentions.


---

## 2. Display-item provisioning assessment

**Verdict: bio-c is adequately provisioned in display-item COUNT (slightly lean but within range), and well-matched in TYPES — with one notable gap for a paper that bills itself as "structure-informed."**

### Count
- bio-c has **4 main figures + 1 table = 5 main display items** (+1 supplementary figure).
- Comparator distribution (n=11): main figures **3–8 (median 6)**; display items **3–9 (median 7)**.
- bio-c's 5 display items sit **below the median (7) but comfortably inside the range** — matched by Ward et al. 2024 (5) and above Belato 2020 / Irisarri 2024 (3–4). **Not under-provisioned; not over-provisioned.** There is clear headroom under GBE's ≤8-display-item Article limit to add one item if warranted (see below), and no case for cutting any.

### Types
Prevalence of each display type across the 11 comparators (papers containing ≥1):

| Type | Papers | bio-c |
|---|--:|---|
| Phylogenetic tree | 9/11 | ✅ Fig 1 (3-domain), Fig 2 (Hfq), Fig S1 (phylum) |
| Quantitative plot (bar/scatter/histogram/distribution) | 8/11 | ✅ Fig 3 (2-panel), Fig 4A |
| Protein-structure panel (3D fold / domain architecture) | 5/11 | ⚠ only indirectly — Fig 4B is a **TM-score histogram**, not a rendered fold |
| Selection plot (dN/dS) | 3/11 | — (not a focus; fine to omit) |
| Synteny / genome alignment | 3/11 | — (not a genome-comparison paper; fine to omit) |
| Schematic / model | 2/11 | — (optional; see note) |

**Reading:** bio-c covers the two dominant display types (trees, quantitative plots) that essentially define this KIND of GBE Article, and its two 2-panel census figures (Fig 3, Fig 4) match the multi-panel convention (comparators average ~3 multipanel figures each; the recent ones — Odelgard 2024 8/8, Luiselli 2024 7/7, Boohar 2023 5/6 — are heavily multi-panel). So the *composition* is right.

**The one gap worth considering.** The paper's framing is "structure-informed," the fold is the protagonist, and the archaeal hits are verified by ESMFold + Foldseek — yet no figure actually **shows** a structure. 5/11 comparators (and the closest structural analogs — Boohar 2023 with 4 structure panels, Saito 2019 with 3, Aidlin Harari 2020 with 3) render the fold in 3D. A single small panel showing (i) the canonical Sm fold with the Sm1/Sm2 motifs labelled, and/or (ii) a representative archaeal ESMFold hit superposed on an experimental anchor (the exact comparison behind Fig 4B's TM-scores), would (a) make the "structure-informed" claim visible rather than asserted, (b) use the available display-item headroom (6 of 8), and (c) bring bio-c in line with the structural comparators. This is an **optional strengthening**, not a deficiency — the science already stands on the census and verification.

**Bottom line:** count is fine (lean side of normal), types are the right ones, and the only substantive suggestion is to consider adding one structural-render panel to cash in the "structure-informed" framing — there is room for it under the display-item cap.

---

## 3. Figure-quality assessment of bio-c's own figures

*Based on opening all five figure files (PNG at 150 dpi + vector PDF) and reading them at native resolution. Judged against GBE production norms and general publication-figure correctness (legibility, multi-panel layout, colour, tree density, labelling).*

### Overall
- **Vector PDFs exist for all figures** — good; this is the correct GBE submission format and sidesteps the 150-dpi PNG resolution issue (the PNGs alone would be below GBE's 300-dpi raster minimum, but the PDFs are resolution-independent).
- **Two production tiers.** Fig 3 and Fig 4 (the census figures) are clean, well-labelled, publication-standard. Fig 1, Fig 2 and Fig S1 (the trees) are the weak point — specifically the two 10 × 26-inch tall Hfq trees.
- **A recurring, easily-fixed issue:** every figure carries an **embedded plot title** (e.g. "Structure-guided Sm/Lsm framework tree (1097 tips), colored by type"). In journal figures the title belongs in the caption, not burned into the image. Remove all in-figure titles.
- **One inconsistency to reconcile:** Fig 1's embedded title says "**1097 tips**" while the text/Methods say the alignment is "**1,101 sequences**." Same object, two numbers (post-dedup vs input). Pick one and state it consistently (and, again, move it to the caption).

### Per-figure

**Figure 1 — three-domain framework tree (circular/fan, 1,097 tips).** *Acceptable, needs polish.*
- Layout is a **circular fan with unlabelled colour-coded tips** — the right choice for 1,097 tips (individual labels would be impossible), and it reads well as a fold-type overview.
- Problems: (i) a **large empty margin** surrounds the tree — the actual ink occupies ~55–60% of the canvas; crop tighter so the tree fills the box. (ii) **Colour scheme is not colour-blind-safe**: the two largest classes, Hfq (red) and Lsm (green), are a red/green pair that deuteranopes cannot separate — and they are the whole point of the figure. Recode to a CVD-safe palette (e.g. Hfq = orange/vermillion, Lsm = blue, Sm-core = yellow, SmAP = purple). (iii) The grey "Other" tips are near-invisible; if they matter, darken; if they don't, say "(unclassified, grey)" in the caption. (iv) Remove the embedded title.

**Figure 2 — rooted Hfq tree, 225 taxa, support concordance.** *Below par as a main figure at its current size — the main thing to fix.*
- Rendered on a **10 × 26-inch canvas** (aspect 2.6 — roughly 3–4 printed pages tall). At GBE's single-column width the 225 tip labels collapse into an **illegible grey fringe**; the four-state support dots survive but the species labels do not. At native resolution the labels *are* readable, but no reader gets native resolution in print.
- The support-concordance encoding (both-high / ML-only / Bayes-only / both-weak dots) is genuinely informative and the legend is clear — the information design is good; the **format is the problem**.
- Concrete fixes, any one of which resolves it: **(a)** move the fully-labelled 225-taxon tree to the **supplement** (as a readable multi-page or large-format PDF) and, in the main text, show a **collapsed/summary version** — collapse well-supported genus/family clades into triangles, keeping ~30–50 leaf groups so labels are legible at column width; **(b)** if all tips must stay, drop per-tip species labels in the main figure and instead **annotate the ~10–15 major clades** with bracket labels (phylum/order), letting the support dots carry the node-level detail; **(c)** at minimum, increase tip-label font and use a **two-column layout** so the tree is ~half as tall. Option (a) is the most GBE-typical.

**Figure 3 — Hfq loss across bacteria (2-panel: A retention-by-lifestyle bar, B presence/absence vs genome size).** *Publication-quality; minor polish only.*
- Clean, well-labelled, panels A/B lettered, blue/red is CVD-safe, counts (n=…) shown on the bars, log x-axis on B is appropriate. This is the model the tree figures should aspire to.
- Optional: in panel B, colour the points by lifestyle (or mark the Actinobacteria/Myxococcus "large-genome-but-absent" points) so the "size-independent lineage loss" message is visible in the figure, not only in the text. Add "n = 71 genomes" to the panel.

**Figure 4 — Sm-fold distribution (2-panel: A retained/lost bar, B TM-score histogram).** *Publication-quality; minor polish only.*
- Panels lettered, retained/lost contrast clear (blue vs red), the TM-score histogram is a sound way to show structural verification.
- Minor: the **annotation text in panel B ("all 55 hits ≥0.92 …") sits close to / slightly over the top bar** — nudge it into clear whitespace. Consider stating "n = 55 hits" once and the median TM as an on-mark tick. The "median 0.97" here must match the text (it does).

**Figure S1 — Hfq tree coloured by phylum (supplementary).** *Acceptable as supplementary.*
- Same 10 × 26-inch tall-tree density as Fig 2, but **as a supplementary figure a full-page portrait tree is acceptable practice**, so the density caveat is much weaker here. Keep it in the supplement (where it already is). The phylum colour legend is clear; the same red/green-adjacent caution applies but matters less for a supplementary overview.

### Would a GBE reader find them at standard?
- **Fig 3, Fig 4, Fig S1: yes.**
- **Fig 1: yes after a recolour + crop + title removal.**
- **Fig 2: not in its current 10×26 form as a main figure** — it needs the collapse/summarise or supplement-plus-summary treatment above. This is the single highest-value figure fix in the paper.

![Tree legibility at print size]({{artifact:art_38e6b409-50ee-49c4-9667-2f58e39f86b7}})

*Left: Fig 2 scaled to ~single-column print width — the 225 tip labels are unreadable. Right: a native-resolution crop showing the labels do exist, but only at the impractical 26-inch full height.*

---

## 4. Comparator papers to emulate (annotated, with DOIs)

*All are GBE Articles, fully open-access. Ordered from closest-in-kind to bio-c downward.*

1. **Boohar et al. 2023.** *Phylogenetic and Protein Structure Analyses Provide Insight into the Evolution and Diversification of the CD36 Domain “Apex” among Scavenger Receptor Class B Proteins across Eukarya* Genome Biol. Evol. — doi:10.1093/gbe/evad218. (6 figs, 0 tables, 80 refs.) **Closest model overall.** Structure-informed phylogeny of an ancient protein family across 165 eukaryotes; shows how to make a 'structure-informed' paper *look* structure-informed — 4 of 6 figures render the fold/ectodomain in 3D. Emulate its structure panels.
2. **Saito et al. 2019.** *Large-Scale Molecular Evolutionary Analysis Uncovers a Variety of Polynucleotide Kinase Clp1 Family Proteins in the Three Domains of Life* Genome Biol. Evol. — doi:10.1093/gbe/evz195. (5 figs, 2 tables, 65 refs.) Protein family across all **three domains** with a presence/frequency census in complete genomes + structural panels — almost exactly bio-c's recipe (tree + cross-domain distribution + structure). Good template for balancing phylogeny, distribution and structure.
3. **Aidlin Harari et al. 2020.** *Molecular Evolution of the Glutathione S-Transferase Family in the Bemisia tabaci Species Complex* Genome Biol. Evol. — doi:10.1093/gbe/evaa002. (6 figs, 1 table, 126 refs.) Protein-family molecular evolution combining phylogeny, **structure models**, and selection; the most heavily-referenced comparator (126). Model for integrating a structural view with sequence evolution.
4. **Irisarri et al. 2024.** *Early Diversification of Membrane Intrinsic Proteins (MIPs) in Eukaryotes* Genome Biol. Evol. — doi:10.1093/gbe/evae164. (3 figs, 0 tables, 65 refs.) **Protein-family diversification + distribution across eukaryotes** with a compact 3-figure set (tree + tree + structure) — another lean, structure-including template close to bio-c's scope.
5. **Belato et al. 2020.** *Evolutionary History of the Globin Gene Family in Annelids* Genome Biol. Evol. — doi:10.1093/gbe/evaa134. (3 figs, 1 table, 100 refs.) A lean **3-figure, all-tree** protein-family phylogeny — proof that a low display-item count passes at GBE when the trees are clean. Useful counterpoint showing bio-c's count is fine.
6. **Odelgard et al. 2024.** *Phylogeny and Expansion of Serine/Threonine Kinases in Phagocytotic Bacteria in the Phylum Planctomycetota* Genome Biol. Evol. — doi:10.1093/gbe/evae068. (8 figs, 0 tables, 62 refs.) **Protein-family phylogeny + lineage-specific expansion census** in a bacterial phylum; 8 heavily multi-panel figures — a model for dense, panel-rich presentation if bio-c wanted to expand (opposite end from Belato).
7. **Brueckner et al. 2020.** *Bacterial Genes Outnumber Archaeal Genes in Eukaryotic Genomes* Genome Biol. Evol. — doi:10.1093/gbe/evaa047. (5 figs, 1 table, 65 refs.) **Cross-domain gene-content census** (bacterial vs archaeal ancestry) — the census/quantitative-distribution half of bio-c, with a clean tree + bar/scatter + schematic sequence. Good model for census figure design.
8. **Gondhalekar et al. 2023.** *Scaling of Protein Function across the Tree of Life* Genome Biol. Evol. — doi:10.1093/gbe/evad214. (6 figs, 2 tables, 76 refs.) **Genome-scale functional census across the tree of life** (bacteria/archaea/eukaryotes) built entirely from quantitative-scaling panels — a model for turning a presence/abundance census into a figure-driven narrative.
9. **Ward et al. 2024.** *Adaptation During the Shift from Entomopathogen to Endosymbiont Is Accompanied by Gene Loss and Intensified Selection* Genome Biol. Evol. — doi:10.1093/gbe/evae251. (5 figs, 0 tables, 97 refs.) **Reduced-genome gene-loss under a lifestyle shift** (pathogen→endosymbiont, 524 gene losses) — the endosymbiont-reduction half of bio-c's story; good model for pairing gene loss with selection and genome context.
10. **Sinha et al. 2023.** *Multiple Lineages of Nematode-Wolbachia Symbiosis in Supergroup F and Convergent Loss of Bacterioferritin in Filarial Wolbachia* Genome Biol. Evol. — doi:10.1093/gbe/evad073. (6 figs, 2 tables, 106 refs.) **Convergent gene-loss** across lineages (bacterioferritin in filarial Wolbachia) — direct analog of bio-c's 'repeated loss' framing; shows how to present loss as the result with phylogeny + synteny + quant support.
11. **Luiselli et al. 2024.** *Genome Streamlining: Effect of Mutation Rate and Population Size on Genome Size Reduction* Genome Biol. Evol. — doi:10.1093/gbe/evae250. (7 figs, 2 tables, 79 refs.) **Genome-reduction mechanism** (streamlining by mutation rate / population size) — the conceptual backdrop to bio-c's reduction gradient; useful for framing the reduction-associated loss mode in the Discussion.

---

## What to act on (priority order)

1. **Add references** to bring the count toward the GBE norm (peer minimum 62, median 79; GBE Article limit is 100). This is the biggest format gap. Purely a breadth-of-citation observation — the specific choices are the author's.
2. **Fix Figure 2** — collapse well-supported clades into triangles for the main-text version and/or move the fully-labelled 225-taxon tree to the supplement. This is the one figure that would not pass at its current 10 × 26-inch size.
3. **Recolour Figure 1** to a colour-blind-safe palette (Hfq red / Lsm green is the critical pair), crop the empty margin, and reconcile "1097 tips" with "1,101 sequences."
4. **Remove embedded plot titles** from all figures (move to captions).
5. **Optional:** add one **structural-render panel** (canonical Sm fold with Sm1/Sm2 motifs, or an archaeal ESMFold hit superposed on its anchor) to make the "structure-informed" framing visible — there is display-item headroom for it.
6. **Minor polish:** Fig 4B annotation clear of the top bar; Fig 3B optionally colour points by lifestyle.

Items 2–6 are format/figure production; item 1 is citation breadth. **None require changing the study's results or claims.**
