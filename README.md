# MYC-Amplification-in-Congenital-Heart-Disease-and-Cancer-in-Kids-First-and-INCLUDE-Data-Set

Using the [Elements of Style in Workflow](https://github.com/NIH-NICHD/Kids-First-Elements-of-Style-Workflow-Creation-Maintenance) creation approach as taught in the https://nih-nichd.github.io, the team will work together to containerize the processing steps and stitch them together in a workflow language.   On [Cavatica](https://www.cavatica.org/), the workflow language best supported is [Common Workflow Language (CWL)](https://www.commonwl.org/).

## Background
[Background Slides](https://docs.google.com/presentation/d/1esjKl4iIlidfSdeqqJ7LwoOxeMA98vDa5TC5pmtq804/edit#slide=id.g2446d821512_0_0)

MYC is an oncoprotein and often implies worse outcomes, however it also seems to have a role in cardiovascular disease. Using open data from both the INCLUDE Data Hub and the Kids First Data Resource Portal, this Hackathon will:

* Explore MYC expression and its segregating effects at the intersection of congenital heart defects and cancer

* Build platform agnostic workflows and analysis notebooks using the elements of style method (https://nih-nichd.github.io) that will use both WGCNA and limma to probe the dual role of this gene.

* Result both in a tutorial of how to proceed from both https://portal.includedcc.org/ and https://portal.kidsfirstdrc.org to https://cavatica.sbgenomics.com/ as well as produce results in notebooks that could be used as figures in a paper promoting open transparent, reproducible results.

## Moving from Portal to Platform …

1. Make two matrices of gene x sample in Cavatica Portal -- in our case the Kids First RNA-seq workflow (pre-made by CHOP) was run first.
2. Combine matrices.
3. Normalize gene expression with deseq2 (not using for differential expression, only for quantile normalisation).
4. Seperate the samples between high and low MYC expression. Gene Median Splitter Docker
5. Classify all subjects by phenotype.
6. Run WGNCA analysis after deciding the binning (what are the "treatments") including High MYC and Low MYC – a template we will move into  a jupyter lab notebook https://bioinformaticsworkbook.org/tutorials/wgcna.html#gsc.tab=0) 
7. Are there drug interactions? Related Repo for [MYC related pediatric drug saftey profiles](https://github.com/BioITHackathons/myc-related-pediatric-drug-safety-profiles)
8. Look at congenital and cardiac impact that might be drug interactions.
9. If outcome (death, etc) is available -- do we see a difference between the two types?
10. What are the outcome differences between high and low MYC expression for the different heart morphologies?
11. Run annotation analysis on the sub-categories -- what are the GO and Pathways? -- maybe run Reactome analysis? -- on the different matrices?

Analysis plan - Weighted Gene Co-expression Network Analysis (WGCNA) [*See Publication*](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-9-559) exists as an R program -> convert to a notebook -> break out the DESeq from the WGCNA

Treatment in the WGCNA sense is the condition of the sample:
* Trisomy and Disomy samples
* High Myc and Low Myc expression.  
* Birth defect (cardiac) and Blood Cancers
* Birth Defect (cardiac) and Solid Tumors

## Docker Files for Project

[Docker File for WGCNA](https://github.com/NIH-NICHD/wgcna-docker)

[Docker File for Gene Median Classifier](https://github.com/NIH-NICHD/gene-median-splitter-docker)

[Docker File for DeSeq2](https://github.com/NIH-NICHD/deseq2-docker)

