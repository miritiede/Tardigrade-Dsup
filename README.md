# Tardigrade Dsup protein
hobby project on the tardigrade protein Dsup using Python 

**Status:** in progress

## Motivation
Tardigrades are micro-animals with the ability to survive extreme conditions such as radiation, desiccation and vacuum. The protein Dsup has been linked to protection of DNA against radiation damage and oxidative stress. This project explores different aspects of Dsup to gain a deeper personal understanding of the molecular processes behind it and to practice Python, scientific thinking and working with literature.

## Research question
| # | Question | Status |
|---|----------|--------|
| 1 | Which regions of Dsup are strongly positively charged and intrinsically disordered, and do they match the regions linked to nucleosome binding in the literature? | In progress |

## Background information on Dsup
Dsup stands for damage suppressor protein, and is according to current findings, unique to the tardigrade species Ramazzoottius varieornatus with only one potential ortholog found in one other species. Dsup is a largely disordered protein, meaning most of it is found in an unfolded state. It is a positively charged protein with a net charge of +23. It is said to protect the DNA from ionizing radiation, which can cause harmful single- or double strand-breaks.  While the exact mechanisms of Dsup are yet to be uncovered, there are findings that inserting the gene encoding Dsup into living cell cultures increases their survival after being exposed to radiation, for example X-rays [1]. 
There are different theories on how Dsup protects the DNA, either directly by binding to the DNA or nucleosomes, dehydrating the DNA or inducing conformational changes in it, or indirectly through forming protein-DNA crosslinks or enhancing the efficiency of DNA repair mechanisms [2].


## Data
- [UniProt Dsup (Ramazzottius varieornatus) amino acid sequence as FASTA file](https://www.uniprot.org/uniprotkb/P0DOW4/history) Entry verion 19; Release number 2026_03/2026_03; Release date 02-Sep-2026
- [UniProt Dsup (Ramazzottius varieornatus) AlphaFold prediction file](https://www.uniprot.org/uniprotkb/P0DOW4/feature-viewer) Downloaded: 29.10.2026
- [UniProt human HMGN2 protein sequence FASTA file](https://www.uniprot.org/uniprotkb/P05204/entry#sequences) Last updated: 2007-01-23 v3
  
See also ./raw_data

## Methods
**Charge profile.** First, the amount of each amino acid contained in Dsup was counted and graphed as an overall overview. Each residue was then assigned +1 (K, R), -1 (D,E) or 0 (all other, including histidine, since it is mostly neutral at pH 7). The amount of the charged residues was graphed as well. The summed charge was computed in a sliding window of 50 residues (step size 1) and plotted at the window center. Window sizes 10, 20, 30, 40, 60, 70 and 100 residues were tested as well. However, is the window size smaller than 50 residues there is too much background noise to see a defined curve, is it bigger the curve gets less detailed. 

**Structure confidence.** Per-residues pLDDT values were read from the B-factor column of the AlphaFold mmCIF file (C-alfa atoms) and plotted. This is only an indirect method of assessing the structural disorder since residues with pLDDT below 50 (very low confidence in the AlphaFold DB classification) are considered to be likely disordered. That means, pLDDT is a confidence measure of the prediciton, not a direct measure of disorder. 

**Software.**

## Results
**Amino acid composition and charge distribution of Dsup**

**Composition.** The 445-residue Dsup sequence is dominated by a small set of amino acids: serine (79), alanine (72), glycine (69) and lysine (59) together make up about 63% of all residues (Figure 1). In contrast, hydrophobic and aromatic residues are very rare: F (2), L (1), M (3), I (4), Y (1), W (0), and cysteine is completely absent. This composition is characteristic of intrinsically disordered proteins, which are enriched in disorder-promoting residues (A, G, S, K, E, P, Q, R) and depleted in order-promoting, hydrophobic and aromatic residues [3]. Small, polar and charged residues keep the chain flexible and soluble, while the bulky hydrophobic residues that normally form a folded core are missing. This fits the reported lack of a defined domain structure in Dsup [2], although disorder is only inferred from the composition here and was not tested directly.
![Amino acid composition of Dsup](figures/fig1_dsup_AS_overview.png)
*Figure 1: Amino acid composition of Dsup (one-letter code).*

**Charge.** Among the charged residues, the positive ones prevail (Figure 2): lysine (59) and arginine (12) give 71 positive charges, aspartate (29) and glutamate (19) give 48 negative charges. The net charge of the full protein is therefore about +23 at neutral pH, ignoring histidine and any modifications. Lysine is the clearly dominant charged residue.
![Charged residues of Dsup](figures/fig2_dsup_chargedAS.png)
*Figure 2: Amount of charged residues in Dsup*

**Local charge distribution.** The sliding window analysis (window size 50, Figure 3) shows that the charge is not distributed evenly along the sequence. The N-terminal part (position ~0–100) is roughly neutral to slightly positive. Around position 150–210 the net charge drops to about −5, which marks a more acidic region. After that, the charge rises again, with a local maximum around position 250 (~+8), a dip near position 290 and a steady increase towards the C-terminus, which reaches the highest value of the whole protein (~+14). The C-terminal region is thus strongly positively charged.
![sliding window analysis](figures/fig3_dsup_window_50_charge.png)
*Figure 3: Sliding window analysis of Dsup local charge distribution*

**Interpretation.** A positively charged, flexible region is well suited to interact with the negatively charged phosphate backbone of DNA. This is consistent with the proposed role of Dsup as a DNA-associated protective protein, where the C-terminal region is thought to be important for binding to chromatin. The charge profile alone does not prove binding or protection, but it supports this hypothesis.

## How to run

## Project structure 

## References
1. Kasianchuk N, Rzymski P, Kaczmarek Ł. The biomedical potential of tardigrade proteins: A review. *Biomed Pharmacother*. 2023 Feb;158:114063. doi: [10.1016/j.biopha.2022.114063](https://doi.org/10.1016/j.biopha.2022.114063). PMID: [36495665](https://pubmed.ncbi.nlm.nih.gov/36495665/).
2. Woodward TJ, Washington MT. Insights into Tardigrade Damage-Suppression Protein, Dsup. *Biomolecules*. 2026 Mar 18;16(3):455. doi: [10.3390/biom16030455](https://www.mdpi.com/2218-273X/16/3/455?utm_source=chatgpt.com). PMID: [41897390](https://pubmed.ncbi.nlm.nih.gov/41897390/); PMCID: PMC13024180.
3. Uversky VN, Gillespie JR, Fink AL. Why are "natively unfolded" proteins unstructured under physiologic conditions? *Proteins.* 2000 Nov 15;41(3):415-27. doi: [10.1002/1097-0134(20001115)41:3<415::aid-prot130>3.0.co;2-7](https://doi.org/10.1002/1097-0134(20001115)41:3%3C415::aid-prot130%3E3.0.co;2-7). PMID: 11025552.

## Use of AI tools
The project idea, the choice of Dsup and the research question are my own. Where possible,
I first tried to find answers myself, for example in the Biopython documentation
(biopython.org) and in the original literature, before asking an AI tool.

I used Claude (Anthropic) as a learning aid and to debug code:
- to refine my ideas
- to fix bugs in my code or get hints on how to proceed 
- to answer technical questions about VS Code, Git and Biopython.
  
The analysis code was written by me, the figures were generated from my own scripts,
and I checked all cited literature myself. Interpretations of the results are my own
and should be read as hypotheses, not as validated findings.

## About
I am a Bachelor's student in Integrated Life Sciences (Biology, Biophysics and Biomathematics) in my third Semester at FAU Erlangen-Nürnberg with an interest in bioinformatics/computational biology. This project is part of my self-directed learning in this area. 

## License
Code is release under the MIT License (see 'LICENSE')


