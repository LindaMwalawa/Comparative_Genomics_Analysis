# De novo Sequence Assembly Using Velvet
De novo sequencing refers to sequencing novel genomes where there are no reference sequences available for alignment. Sequence reads are then assembled into contigs, with the coverage quality of de novo sequence data depending on the size and continuity of the contigs (ie, the number of gaps in the data).
Velvet is one of several de novo assemblers designed to process short-read datasets, such as Illumina reads, utilizing de Bruijn graphs as the foundation for its assembly method.

## How it works
De novo genome assembly involves the following main steps:

1. Fragmentation of DNA:
   - The genome is fragmented into millions of small pieces, which are sequenced using platforms like Illumina or PacBio to produce short reads (tens to hundreds of base pairs long) or 
    long reads (up to several kilobases for some technologies).

2. Read Overlap Identification:
   - The velvet assembler identifies overlaps between sequencing reads by constructing a de Bruijn graph, where reads are broken into smaller units (k-mers) to find 
    connections.

3. Assembly of Contigs and Contigs formation:
   - Overlapping reads are merged into longer continuous sequences called contigs which are ordered and oriented into larger structures called scaffolds using information from paired- 
    end or mate-pair reads.

4. Gap Filling and Polishing:
   - Gaps in scaffolds are filled where possible, and assembly errors are corrected using additional sequencing data or computational tools.

## Sequence assembly workflow
For this exercise, paired end reads from an unidentified organism were downloaded as a zipped folder from an open source and quality control done using Trimmomatic to remove bases of low quality (phred score < 33). By default, Velvet comes with a maximum k-mer length of 31 hardcoded into the Makefile, however for this exercise, this value was adjusted to 71. Two key programs, velveth and velvetg are used in the velvet pipeline for genome assembly, each serving distinct purposes. Velveth is responsible for preparing the dataset for assembly by creating hash tables and building the de Bruijn graph while velvetg takes the output from velveth and performs the actual assembly by manipulating the de Bruijn graph. The output data was then blasted in the BLASTN tool in NCBI and the predicted result of Myotis brandtii angiotensin I converting enzyme 2 (ACE2) was obtained.
