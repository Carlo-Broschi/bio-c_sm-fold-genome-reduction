# Submission-format versions of the bio-c manuscript

Two journal-formatted versions of the integrated manuscript are provided. The
**science is identical**; only the formatting differs. The canonical source is the
repository `draft.md`; these are assembled views for two candidate venues.

| | `gbe/` | `jme/` |
|---|---|---|
| Journal | Genome Biology and Evolution (Article) | Journal of Molecular Evolution |
| Section order | Methods **at the end** (GBE convention) | Methods **after Introduction** (standard) |
| Front matter | **Significance statement** (GBE-required) | **Keywords** (6, Springer) |
| In-text citations | author–date `(Author year)` | author–year `(Author year)` — same |
| Reference list | GBE author–date, ≤5 authors listed else et al.; sentence-case titles | Springer name–year, **first 3 authors + "et al" (no period)**, `(year)`; ISO-abbreviated journal names |
| Access model | fully open access (APC) | hybrid (subscription route = no APC; work is already green-OA via the bioRxiv preprint + Zenodo) |

## Files
- `gbe/bioc_gbe_manuscript.md`, `gbe/bioc_gbe_references.md`
- `jme/bioc_jme_manuscript.md`, `jme/bioc_jme_references.md`

## Finalisation before upload (either venue)
1. **References** — both lists are DOI-verified drafts. Produce the final list with a
   reference manager (Zotero/EndNote) using the journal's CSL/style: the GBE style for
   the GBE version, the Springer *Journal of Molecular Evolution* (Basic) style for the
   JME version — this applies the journal's exact author-truncation rule, title case, and
   (for JME) ISO journal-name abbreviations automatically. `../refs.bib` imports directly.
2. **Figures** — Fig 1–5 (+ Fig S1) are in `../4-results/`; convert to the journal's
   raster spec at upload (e.g. CMYK 300 dpi TIFF for GBE). Figure legends are in the
   manuscript; upload figures as separate files.
3. **Supplementary Table S1** — `../supplementary_table_S1.md` (19 structural anchors).
4. **bioRxiv** — post the preprint (`../preprint/bioc_preprint.pdf`) and do a last
   keyword check ("Hfq DPANN", "Sm fold CPR") for claim (c) before journal submission.

**JME specifics applied** (per Springer guidelines, journal 239): research Article (~4,400 words body; JME Short Reviews are <3,000 words); Springer name–year references (first 3 authors + "et al", no period — verified against a recent JME article); a Springer **Statements and Declarations** block with a **Conflict of interest** heading (Funding / Conflict of interest / Ethics approval / Author contributions / Data availability / Use of generative AI). Springer figure spec at upload: ≥300 dpi halftone, 600 dpi combination, TIFF/EPS/PDF.

The author remains responsible for the content of both versions (see the AI-use
disclosure in the manuscript Declarations).
