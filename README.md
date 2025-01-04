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

## Installation

Choose the installation method based on your system architecture.

### Standard Installation (Windows/Linux/Intel Mac)

Create and activate a conda environment:

```sh
conda create -n variant_analysis
conda activate variant_analysis
```




Install all required tools:
```sh
conda install -c bioconda -c conda-forge gatk samtools bwa bcftools snpeff
```



### Apple Silicon (M1/M2)

Configure environment and channels:

```sh
conda create -n gatk_pipeline
conda activate gatk_pipeline

conda config --add channels defaults
conda config --add channels bioconda
conda config --add channels conda-forge
```

Install tools individually:

```sh
conda install -c bioconda -c conda-forge samtools
conda install -c bioconda -c conda-forge bwa
conda install -c bioconda -c conda-forge bcftools
conda install -c bioconda -c conda-forge snpeff
conda install -c bioconda -c conda-forge openjdk=8
conda install -c bioconda gatk4
```

#### Verify Installation

Check if all tools are installed correctly:

```sh
samtools --version
bwa
bcftools --version
gatk --list
snpEff -version

```



