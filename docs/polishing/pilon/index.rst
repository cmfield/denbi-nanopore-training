Assembly polishing with pilon
=============================

Pilon is a software tool which can be used to automatically improve draft assemblies or to find variation among strains, including large event detection.
Pilon requires as input a FASTA file of the genome along with one or more BAM files of reads aligned to the input FASTA file. Pilon uses read alignment analysis to identify inconsistencies between the input genome and the evidence in the reads. It then attempts to make improvements to the input genome, including:

- Single base differences
- Small indels
- Larger indel or block substitution events
- Gap filling
- Identification of local misassemblies, including optional opening of new gaps

Pilon then outputs a FASTA file containing an improved representation of the genome from the read data and an optional VCF file detailing variation seen between the read data and the input genome.

To aid manual inspection and improvement by an analyst, Pilon can optionally produce tracks that can be displayed in genome viewers such as IGV and GenomeView, and it reports other events (such as possible large collapsed repeat regions) in its standard output.
More information on pilon can be found here:
https://github.com/broadinstitute/pilon/wiki


We have prepared a set of Illumina data for you, which we are now using for polishing with pilon::

  ls -l ~/workdir/Data/Illumina/
  
  total 726604
  -rw-r--r-- 1 ubuntu ubuntu       432 Nov  7 08:55 assembly_stats.txt
  -rw-r--r-- 1 ubuntu ubuntu  28924964 Nov  7 08:55 MP2.fastq.fwd
  -rw-r--r-- 1 ubuntu ubuntu  29457256 Nov  7 08:55 MP2.fastq.rev
  -rw-r--r-- 1 ubuntu ubuntu  15943849 Nov  7 08:55 MP2.fastq.uni
  -rw-r--r-- 1 ubuntu ubuntu 315258550 Nov  7 08:55 TSPf_R1.fastq.gz
  -rw-r--r-- 1 ubuntu ubuntu 354446667 Nov  7 08:55 TSPf_R2.fastq.gz
  


.. toctree::
 :maxdepth: 1

 extract
 mapping
 pilon
 quast
 mapping_assembly2reference
 
References
^^^^^^^^^^

**pilon** https://github.com/broadinstitute/pilon
