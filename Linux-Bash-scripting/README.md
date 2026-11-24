# HackBio Internship - Stage Zero: Bash & Bioinformatics Setup

This repository contains the bash scripts and command logs for **Stage Zero** of the HackBio Internship. The projects focus on fundamental Linux command-line operations for biological data manipulation and setting up a reproducible bioinformatics environment using Conda.

## 📂 Repository Contents

* **`stage-zero_Project 1.txt`**: A Bash script demonstrating basic directory navigation, file downloading, sequence pattern searching (`grep`), and parsing GenBank (`.gbk`) and FASTA (`.fna`) files.
* **`stage-zero_Project_2.txt`**: A Bash script for setting up a dedicated Conda environment (`funtools`) and installing essential bioinformatics and NGS (Next-Generation Sequencing) tools.

---

## 🛠️ Project Breakdown

### Project 1: Basic Bash & Sequence Analysis
This script performs foundational file management and text-processing tasks on biological sequence files:
* **Workspace Setup**: Creates project directories (`manju` and `biocomputing`) and downloads sample `wildtype.fna` and `wildtype.gbk` files from the HackBio repository.
* **Mutant Identification**: Uses `grep` to search for specific TATA-box motifs (`tata` vs. `tatatata`) within the FASTA file and isolates mutant sequences into a separate `mutant.fna` file.
* **GenBank Parsing**: Extracts key metadata from `wildtype.gbk` using `awk`, `cut`, `head`, `tail`, and `wc`:
  * Counts total lines excluding the header.
  * Extracts the sequence length from the `LOCUS` line.
  * Identifies the `SOURCE` organism.
  * Lists all unique `/gene=` annotations.

### Project 2: Bioinformatics Environment Setup
This script automates the creation of a Python 3.10 environment and installs standard command-line utilities and bioinformatics packages via `apt-get` and the `bioconda` channel:
* **Environment**: `funtools` (Python 3.10, `pandas`, `numpy`)
* **System Utilities**: `figlet`
* **Bioinformatics Tools**:
  * **Alignment & Mapping**: `bwa`, `blast`
  * **Sequence & Variant Manipulation**: `samtools`, `bedtools`, `bcftools`
  * **Genome Assembly**: `spades`
  * **Quality Control**: `fastp`, `multiqc`

---
