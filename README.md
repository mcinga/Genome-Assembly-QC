# Genome Assembly QC Pipeline
This nexflow pipeline is to assess the quality of de novo genome assemblies for human genome assembly, created from long read sequencing data. This includes PacBio HiFi, Oxford nanopore (ONT) ultra-lond data and Omni-C/HiC or trio data.
However, it can be modified to cater for other species. The quality of the assemblies is assessed by measuring continuity, correctness and completness.
Continuity is assessed using the latest version of gfastats, correctness (QV value) is asssed using Merqury which is  km-er based technique. Completness is futhermore assesed using BUSCO.

Each haplotype is assessed independently.    
## Requirements
- Nextflow
- Singularity
## Input structure
Ensure that all the assemblies are in one directory, and the reads are in one directory.
Both assemblies an reads should follow the format below and have a sample ID as an identifier as seen below.
```
assemblies/
|-KRM.hap1.fasta
|-KRM.hap2.fasta

reads/
|-KRM.fastq.gz
```
## Running the pipeline
Create a bash script and add the following:
```
module load nextflow
module load singularity 

nextflow run main.nf -profile slurm 

```
## Notes

