# bio-c: The Fate of the Sm Fold under Genome Reduction

## Project
**Title:** The fate of the Sm fold under genome reduction: a structure-informed phylogeny across the three domains of life  
**Venue:** JME（第一候補・APC ¥0）→ 落ちたら GBE  
**Zenodo:** 10.5281/zenodo.21202213  
**Status:** 投稿準備完了（bioRxiv/Zenodo 公開済み・投稿料が貯まり次第・年内目標）  
**GitHub:** `Carlo-Broschi/bio-c_sm-fold-genome-reduction`（Public, v1.0.0）

## 統合の経緯
bio-a（Hfq系統解析）+ bio-b（Sm/Lsm系統解析）を 2026-07-05 に統合。  
bio-a DOI: 10.5281/zenodo.21197822、bio-b DOI: 10.5281/zenodo.21197824（Data Availabilityに相互記載済み）

## Paper Structure
- **Framework**: 3ドメイン構造ガイド木 + Hfq dual-method 94.5%一致
- **Finding 1**: 細菌 Hfq 二重モード喪失 + CPR 0/397
- **Finding 2**: 古細菌保持 55/55 構造検証（ESMFold + foldseek TM 0.918–0.999）
- **Synthesis**: ドメイン非対称（細菌喪失 vs 古細菌保持）
- **Stats**: 48件引用・本文約4,400語・Fig 1–5 + Supplementary Table S1

## Key Numbers
| 指標 | 値 |
|---|---|
| ML vs Bayes 一致率（UFBoot≥95） | 94.5%（86/91枝） |
| DPANN/Asgard Sm/Lsm保持 | 55/55（foldseek TM中央値0.967） |
| CPR Sm/Lsm | 0/397 |
| Hfq喪失相関 r（Actinobacteria除外） | r=0.51 |
| bio-a ASDSF（MrBayes） | 0.0468 |

## Paper Collection
`Research/Biology/bio-c/`

コンテキストファイル: `Research/Biology/bio-c/_context_生物C.md`  
（生成: `uv run python agent.py --context=生物C`）

## Key References
- Veretnik et al. 2009 (PLoS CB) — 主な更新対象
- Sun, Zhulin & Wartell 2002 (NAR 30:3662) — Hfq喪失の一次文献
- Reichelt et al. 2023 (Biol. Chem. 404:1085) — PfuSmAP1機能（=Grohmann 2023）
- Kambach et al. 1999 (Cell 96:375) — Smフォールド定義・PDB 1D3B/1B34
- Wong et al. 2026 — IQ-TREE3（Minh 2020はIQ-TREE2、使わない）
- Gilchrist et al. 2026 (Science 391:485) — FoldMason

## Remaining Actions（著者本人）
- 構造ガイド IQ-TREE 独立再推定（UFBoot 43% 再現確認済み）
- draft通読（各主張を自分の言葉で説明できるか）
- bioRxiv キーワード最終確認（"Hfq DPANN"・"Sm fold CPR"）
