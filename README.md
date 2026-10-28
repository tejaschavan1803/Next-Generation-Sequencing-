# NGS Pipeline for Driver Mutation and CNV Analysis in Uveal Melanoma

## Project Overview

This project analyzes publicly available Next-Generation Sequencing (NGS) data to explore genomic variations associated with uveal melanoma. The workflow includes data retrieval, quality control, read preprocessing, reference genome alignment, alignment file processing, and genomic visualization.

## Pipeline Workflow

```text
Public NGS Data
      |
      v
NCBI Sequence Read Archive (SRA)
      |
      v
Download FASTQ Files
      |
      v
Quality Control
     FastQC
      |
      v
Read Preprocessing
     fastp
      |
      v
Reference Genome Alignment
     BWA + GRCh38
      |
      v
Alignment File Processing
     SAMtools
      |
      v
Workflow Organization and Processing
     Galaxy
      |
      v
Genomic Visualization
     IGV
      |
      v
Exploration of Genomic Variations
and Potential CNV Patterns
```

## Tools and Technologies

| Tool     | Purpose                                               |
| -------- | ----------------------------------------------------- |
| NCBI SRA | Retrieval of publicly available sequencing data       |
| FASTQ    | Storage of raw sequencing reads and quality scores    |
| FastQC   | Assessment of sequencing read quality                 |
| fastp    | Adapter trimming and low-quality read filtering       |
| BWA      | Alignment of sequencing reads to the reference genome |
| GRCh38   | Human reference genome assembly                       |
| SAMtools | Processing and management of SAM/BAM alignment files  |
| Galaxy   | Management of bioinformatics workflow steps           |
| IGV      | Visualization of aligned reads and genomic regions    |

## Pipeline Steps

### 1. Data Retrieval

* Retrieved publicly available NGS sequencing data from the NCBI Sequence Read Archive (SRA).
* Used FASTQ files as input for downstream analysis.

### 2. Quality Control

* Used FastQC to inspect read quality, sequence quality scores, adapter content, and other sequencing quality metrics.

### 3. Read Preprocessing

* Used fastp for adapter trimming and filtering of low-quality reads.
* Prepared processed reads for reference genome alignment.

### 4. Reference Genome Alignment

* Aligned processed sequencing reads to the human reference genome GRCh38 using BWA.
* Generated alignment output for downstream processing.

### 5. Alignment File Processing

* Used SAMtools to manage and process SAM/BAM alignment files.
* Prepared alignment data for visualization and downstream inspection.

### 6. Workflow Management

* Used Galaxy to organize and execute relevant bioinformatics workflow steps.

### 7. Genomic Visualization

* Used Integrative Genomics Viewer (IGV) to inspect aligned reads and genomic regions of interest.
* Explored genomic variation and potential copy-number variation (CNV) patterns.

## Project Scope

This project demonstrates a basic NGS analysis workflow, from raw sequencing data quality assessment to reference genome alignment and visualization. It provides practical exposure to sequencing quality control, read preprocessing, genome alignment, alignment file handling, and genomic data interpretation.

**Note:** Dedicated variant calling and CNV detection require appropriate downstream tools and analyses. Visualization alone does not confirm driver mutations or establish CNV calls.
