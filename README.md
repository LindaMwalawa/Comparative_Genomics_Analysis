# Comparative ACE2 Analysis: Investigating Viral Binding Sites Across Species 

The workflow involved the following
1. Quality Control of raw reads
2. De novo genome assembly
3. Validation of assembled sequence
4. Multiple sequence alignment
5. Determination of evolving sites across species

## Objective:

To investigate evolving sites within the ACE2 gene across different species, particularly those affecting viral binding to SARS-CoV and SARS-CoV-2

## Tools Used
1. FastQC
2. Trimmomatic
3. Velvet (velveth & velvetg)
4. NCBI BLAST
5. ClustalO
6. AliView
7. IQTREE
8. iTOL
9. PDB

## De novo Assembly Workflow
1. Download raw sequencing reads
2. Quality assessment of reads
3. Trim low-quality sequences
4. Perform de novo genome assembly
5. Validate assembly in BLAST
6. Download ACE2 sequences from other species
7. Append the top hit from NCBI to multiple sequences
8. Align sequences
9. Generate a phylogenetic tree
10. Visualize the tree
11. Detect evolving sites
14. Compare with viral binding residues
15. Assess protein 3D structures

