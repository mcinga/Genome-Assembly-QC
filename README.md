# Genome Assembly QC Pipeline
This nexflow pipeline is to assess the quality of de novo genome assemblies specific for hman genome assembly.
However, it can be modified to cater for other species.The quality of the assemblies is done continuity, correctness and completness.
Continuity is assessed using the latest version of gfastats, correctness (QV value) is asssed using Merqury which is  km-er based technique. Completness is futhermore assesed using BUSCO.

Each haplotye is assessed independetly.    
## Requirements
- Nextflow
- Singularity
## Input structure
```
assemblies/
|-assembly.hap1.fasta
|-assembly.hap2.fasta

reads/
|-read.fastq.gz
```
## Running the pipeline

## Notes
- Each haplotype is processed independently
