Indexing fastq from 1D Basecalling
----------------------------------

In order to prepare our 1D fastq file for nanopolish (so that the tool can find the original raw files), we need to index the fastq files from the 1D basecalling again with nanopolish::

  nanopolish index -d ~/workdir/Data/Nanopore/ ~/workdir/Results/1D_basecall.fastq
