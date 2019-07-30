---
date: 2019-06-11T02:16:24+08:00
author:
  name: "Pei-Wen Shih"
emoji: true
linktitle: SOP of bacteria sequencing analysis 
tags:
- sequencing analysis
title: SOP of bacteria sequencing analysis
weight: 10
series: note
toc : false
---

1. Quality control

   - QC tools ([FastQC](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/), [MultiQC](https://multiqc.info/) ...)

   - Is coverage enough ?

   - Is length  read length enough ? 

   - Is there contamination ?

2. Assembly

   - Assembler tools ([Canu](https://canu.readthedocs.io/en/latest/quick-start.html), [Unicycler](https://github.com/rrwick/Unicycler), [Flye](https://github.com/fenderglass/Flye), [Ra](https://github.com/lbcb-sci/ra) …)

   - Genome Polishing ([Racon](https://github.com/isovic/racon),  [medaka](https://nanoporetech.github.io/medaka/index.html), [nanopolish](https://nanopolish.readthedocs.io/en/latest/quickstart_consensus.html) ...)

   - Plasmid check([BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi))

3. Genome annotation

   - NCBI annotation

   - COG analysis for protein functions

4. 16S rRNA/whole genome phylogenetic trees 

5. Antibiotic-resistant gene prediction

6. Virulence gene prediction