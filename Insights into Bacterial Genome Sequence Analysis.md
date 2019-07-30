---
author:
  name: "Pei-Wen Shih"
date: 2019-06-07 09:00:00
emoji: true
linktitle: Insights into Bacterial Genome Sequence Analysis
tags:
- genome assembly
- third generation sequence
title: Insights into Bacterial Genome Sequence Analysis
weight: 10
series: Summer training
toc : true
---

# Today goals

* Introduction - A little about me, lab(~~gossip~~)

* Things you should know before assembly
  1. Fastq format
  2. Fasta format
  3. GC- content
  4. Status of genome
* Step to bacterial sequencing analysis

# Introduction - A little about me, lab(~~gossip~~)

名字： 施佩妏 :smile:

興趣：看美劇、實況、吃雞肉飯

畢業前目標：把嘉義雞肉飯吃一遍

Lab ~~淺~~規則：兩週報一次、問問題

# Things you should know before assembly

## Fastq format

```
@cc3e68c4-b53d-43da-be7e-b961113007e2          -> sequence name
ATCCGGAATCGGTTACTGTTGGGAACCTTTGC               -> sequence
+                                              -> quality line break
#%(*))++.2/148447;7+001./18-7-,,30&*2          -> quality score
```

## Fasta format

```
>tig00000001				           -> sequence name
TGATAAAAGTATTCATATAATCTCCTATCATTTCAAAATTTAAT   -> sequence 
>tig00000002																	 
ATATTAGTGTGTCTATTTTATGGGGCTAGGAAAGGAGGTACATT
```

## GC-content

 the percentage of [nitrogenous bases](https://en.wikipedia.org/wiki/Nitrogenous_bases) on a [DNA](https://en.wikipedia.org/wiki/DNA) or [RNA](https://en.wikipedia.org/wiki/RNA) molecule that are either [guanine](https://en.wikipedia.org/wiki/Guanine) or [cytosine](https://en.wikipedia.org/wiki/Cytosine)
$$
\frac{G+C}{A+T+G+C} \times 100 \%
$$

## Satuts of genome

![Alt text](http://ecoevo.unit.oist.jp/lab/wp-content/uploads/2013/08/GenomeAssembly.png)

### 1. contig

   A **contig**  is a set of overlapping DNA segments that together represent a [consensus region of DNA](https://en.wikipedia.org/wiki/Consensus_sequence).

### 2. scaffold

  To bridge the gaps between the two contigs called scaffold.

### 3. complete

  ​A **circular** genome

![Alt text](https://albertsenlab.org/wp-content/uploads/2017/11/longreadsVSshortreads.png)

# Step to bacterial sequencing analysis

![Alt text](https://f1000researchdata.s3.amazonaws.com/manuscripts/14771/860b5457-c42e-40df-9829-10ecb2c4b092_figure2.gif)

## Step 1. Quality Control - Assessing the quality of TGS (Third Generation Sequencing)

### 1.1 Checking raw read statistics

Tools : [abyss-fac](https://github.com/bcgsc/abyss)

![Imgur](/Users/spaert/Documents/mysite/blog/content/posts/img/read-abyssfac.png)

* n : Number of raw read

* N50 : A value that present 50% of sorted read set

  ![Alt text](https://i0.wp.com/www.molecularecologist.com/wp-content/uploads/2017/03/Figure1b.jpg?w=699&ssl=1)

* Max: longest read length

* Sum: Total read length

### 1.2 QC report

Tools : [FastQC](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/)

Input : Fastq

