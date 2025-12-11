# PGRR: Pangenome Gene Reference Resource

The **Pangenome Gene Reference Resource (PGRR)** is a comprehensive pangenome of the _M. tuberculosis complex_ (MTBC), which spans all seven _M. tuberculosis_ lineages and is produced  using a virtually error-free sequencing and de novo assembly approach. It encompasses the complete panorama of genetic variation across all genes present in _M. tuberculosis_ to provide an efficient tool for performing isolated gene alignments and for accessing gene-level information from the pangenome reference strains.

## Instructions for Use

Align your query reads to the PGRR using a standard sequencing alignment tool, such as [Bowtie2](https://bowtie-bio.sourceforge.net/bowtie2/index.shtml) or [bwa](https://github.com/lh3/bwa?tab=readme-ov-file). Be sure to set the PGRR fasta file as the reference. An example bash script can be found below:

```
# Align a paired read to PGRR
module load bowtie2
bowtie2 --no-unal -x PGRR.fasta -1 $forward_read -2 $reverse_read --very-sensitive-local -S $result.sam
```

## Citation

Poonam Chitale, Elissa Ocke, Aubrey R. Odom, Howard Fan, Alexander Henoch, Karla Vasco, Emily C. Fogarty, Courtney Grady, Alexander D. Lemenze, Pradeep Kumar, Shannon Manning, A. Murat Eren, W. Evan Johnson, and David Alland. Defining the Mycobacterium tuberculosis Pangenome and Suggestions for a New Composite Reference Sequence.
