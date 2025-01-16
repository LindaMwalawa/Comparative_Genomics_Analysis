# De Novo Assembly and Multiple Sequence Alignment ACE2 Gene in Bats and Humans.
The workflow involved the follwoing steps

## De novo Assembly of ACE2 using velvet

1. Qaulity control of paired end reads using Fastqc
2. Trimming adapater sequences and removing low quality bases (Phred >33)using Trimmomatic
3. Assembly of the Qcied reads using velveth and velvetg
4. Validation and orientation of consensus contigs in NCBI (Top hit matched the Myotis brandtii bat species) 

## Evolutionary analysis of assembled ACE2 contigs in Bats and Humans
1. Downloading ACE2 sequences of 4 other bat species (Myotis lucifungus, Myotis davidii, Myotis myotis and Eptesicus fuscus)
2. Downloading human ACE2 sequence data from NCBI (ACE2, transcript variant 1, mRNA)
3. Concatenating ACE2 contigs from Myotis brandtii with the ACE2 genes from the 4 bat species and humans 
4. Performing alignment of the sequences using ClustalO
5. Visualization the multiple sequence alignment using Aliview
6. Phylogenetic tree generation using IQTREE
7. Visualize Tree: Use the iTOL website to view the phylogenetic tree: https://itol.embl.de/upload.cgi.
8. Combine Alignment and Tree: Use cat New_ACE2.fa.aln New_ACE2.fa.aln.treefile >CombinedACE2species.fa to combine the alignment and tree file
9. Run MEME Analysis: Upload the combined file to the Datamonkey MEME server (Set p-value Threshold: Change the p-value threshold to 0.05)
10. Export results to a CSV file, copy the "sites" and "p-value" columns, and use the FDR tool to adjust for multiple testing: https://tools.carbocation.com/FDR.
11. Identifying Evolving Sites


## Identify Significant Sites: Identify alignment sites with significant positive selection.
●
Correlate with Unaligned Sites: View the alignment in AliView to determine the unaligned amino acid position for each significant site.
11. Protein Structure Analysis
●
Access PDB: Go to the Protein Data Bank (PDB) at https://www.rcsb.org.
●
Find 3D Structure: Find the structure for "6m0j" and view its features in 3D.
●
Explore Binding Sites: Rotate the molecule to view where ACE2 and spike bind.
●
Compare Sites: Compare the key binding sites to the sites under selection
   
