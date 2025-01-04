# GATK-Based-Variant-Calling-and-Analysis-on-Chromosome-17 (in progress)

This repository contains a comprehensive pipeline for germline variant calling and analysis using the Genome Analysis Toolkit (GATK). The project focuses on chromosome 17, one of the most gene-dense regions of the human genome that houses critical genes including BRCA1, TP53, and ERBB2 (HER2), using exome data from 27 samples from the 1000 Genomes Project. The pipeline integrates robust bioinformatics workflows for data preprocessing, variant discovery, and annotation to explore the genetic variations and their potential biological impacts.


## Workflow
The analysis pipeline is structured into three main phases:

### Pre-Processing:

Data retrieval of chromosome 17 exome alignments.
BAM file quality control and alignment to the GRCh38 reference genome.
Removal of duplicates and base quality score recalibration (BQSR).


### Variant Discovery:

Identification of single nucleotide polymorphisms (SNPs) and INDELs using GATK's HaplotypeCaller.
Joint genotyping of all samples to produce a cohort VCF file.


### Callset Refinement and Annotation:

Variant Quality Score Recalibration (VQSR) to filter high-confidence variants.
Annotation using snpEff to classify variants based on genomic impact and functional categories.
Special focus on variants in cancer-associated genes and their regulatory regions.
