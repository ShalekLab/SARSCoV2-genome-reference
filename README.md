# SARSCoV2-genome-reference
Edited SARS-CoV-2 genome fasta and gtf for Ziegler et al. 2021

Modified SARS-CoV-2 FASTA and GTF file for scRNA-seq alignments as described in Ziegler et al. 2021

Original genome reference: Kim et al. "The Architecture of SARS-CoV-2 Transcriptome" Cell 2020

Brief description of modifications:
A custom reference was created by combining human GRCh38 (from CellRanger version 3.0.0, Ensembl 93) and SARS-CoV-2 RNA genomes. The SARS-CoV-2 viral sequence and GTF are as described in Kim et al. 2020 (https://github.com/hyeshik/sars-cov-2-transcriptome, BetaCov/South Korea/KCDC03/2020 based on NC_045512.2). The GTF includes all CDS regions (as of this annotation of the transcriptome, the CDS regions completely cover the RNA genome without overlapping segments), and regions were added to describe the 5’ UTR (“SARSCoV2_5prime”), the 3’ UTR (“SARSCoV2_3prime”), and reads aligning to anywhere within the Negative Strand (“SARSCoV2_NegStrand”). Trailing A’s at the 3’ end of the virus were excluded from the SARS-CoV-2 FASTA, as these were found to drive spurious viral alignment in pre-COVID19 samples. Finally, additional small sequences were appended to the FASTA and GTF that differentiate reads that align to the 70-nucleotide region around the viral TRS sequence – either across the intact, unspliced genomic sequences (e.g. named “SARSCoV2_Unspliced_S” or “SARSCoV2_Unspliced_Leader”) or various spliced RNA species (e.g. “SARSCoV2_Spliced_Leader_TRS_S”)
