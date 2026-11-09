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
1. Downloaded the amino acid sequence of *Ramazzottius varieornatus*
2. Wrote first script to read the FASTA, get the sequence length and the number of each amino acid

## Results
*coming soon (hopefully)*

## How to run

## Project structure 

## References
1. Kasianchuk N, Rzymski P, Kaczmarek Ł. The biomedical potential of tardigrade proteins: A review. *Biomed Pharmacother*. 2023 Feb;158:114063. doi: [10.1016/j.biopha.2022.114063](https://doi.org/10.1016/j.biopha.2022.114063). PMID: [36495665](https://pubmed.ncbi.nlm.nih.gov/36495665/).
2. Woodward TJ, Washington MT. Insights into Tardigrade Damage-Suppression Protein, Dsup. *Biomolecules*. 2026 Mar 18;16(3):455. doi: [10.3390/biom16030455](https://www.mdpi.com/2218-273X/16/3/455?utm_source=chatgpt.com). PMID: [41897390](https://pubmed.ncbi.nlm.nih.gov/41897390/); PMCID: PMC13024180.

## About
I am a Bachelor's student in Integrated Life Sciences (Biology, Biophysics and Biomathematics) in my third Semester at FAU Erlangen-Nürnberg with an interest in bioinformatics/computational biology. This project is part of my self-directed learning in this area. 

## License
Code is release under the MIT License (see 'LICENSE')


