# Genome Assembly QC Pipeline
This nexflow pipeline is to assess the quality of de novo genome assemblies for human genome assembly, created from long read sequencing data. This includes PacBio HiFi, Oxford nanopore (ONT) ultra-lond data and Omni-C/HiC or trio data.
However, it can be modified to cater for other species. The quality of the assemblies is assessed by measuring continuity, correctness and completness.
Continuity is assessed using the latest version of gfastats, correctness (QV value) is asssed using Merqury which is  km-er based technique. Completness is futhermore assesed using BUSCO.

Each haplotye is assessed independetly.    
## Requirements
- Nextflow
- Singularity
## Input structure
Ensure that all the assemblies are in one directory, and the reads are in one directory.
```
assemblies/
|-assembly.hap1.fasta
|-assembly.hap2.fasta

reads/
|-read.fastq.gz
```
## Running the pipeline
Create a bash script:
```
module load nextflow/25.10.0 
module load singularity/4.2.2 

nextflow run quality_control.nf -profile slurm 

```
## Notes

