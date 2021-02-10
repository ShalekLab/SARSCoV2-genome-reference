# SARSCoV2-genome-reference

Modified SARS-CoV-2 FASTA and GTF file for scRNA-seq alignments as described in Ziegler et al. 2021

Original genome reference: Kim et al. "The Architecture of SARS-CoV-2 Transcriptome" Cell 2020

A custom reference was created by combining human GRCh38 (from CellRanger version 3.0.0, Ensembl 93) and SARS-CoV-2 RNA genomes. The SARS-CoV-2 viral sequence and GTF are as described in Kim et al. 2020 (https://github.com/hyeshik/sars-cov-2-transcriptome, BetaCov/South Korea/KCDC03/2020 based on NC_045512.2). The GTF includes all CDS regions (as of this annotation of the transcriptome, the CDS regions completely cover the RNA genome without overlapping segments), and regions were added to describe the 5’ UTR (“SARSCoV2_5prime”), the 3’ UTR (“SARSCoV2_3prime”), and reads aligning to anywhere within the Negative Strand (“SARSCoV2_NegStrand”). Trailing A’s at the 3’ end of the virus were excluded from the SARS-CoV-2 FASTA, as these were found to drive spurious viral alignment in pre-COVID19 samples. Finally, additional small sequences were appended to the FASTA and GTF that differentiate reads that align to the 70-nucleotide region around the viral TRS sequence – either across the intact, unspliced genomic sequences (e.g. named “SARSCoV2_Unspliced_S” or “SARSCoV2_Unspliced_Leader”) or various spliced RNA species (e.g. “SARSCoV2_Spliced_Leader_TRS_S”). Genome was built for either 10X libraries using https://cumulus.readthedocs.io/en/stable/cellranger.html (cumulus/cellranger_create_reference snapshot 8) or Seq-Well (dropseq structure) libraries using https://cumulus.readthedocs.io/en/stable/drop_seq.html (cumulus/dropseq_bundle snapshot 4).


Files:

1. SARSCoV2_v5.fa - fasta containing only the viral regions
2. SARSCoV2_v5.gtf - gtf matching the viral fasta


![](https://github.com/ShalekLab/SARSCoV2-genome-reference/blob/main/Github_Genome_SARSCoV2_Schematic.png)


Contact Carly Ziegler (cziegler@mit.edu), Jose Ordovas-Montanes (jose.ordovas-montanes@childrens.harvard.edu), or Alex Shalek (shalek@mit.edu) with any questions
