# MYC-Amplification-in-Congenital-Heart-Disease-and-Cancer-in-Kids-First-and-INCLUDE-Data-Set

Using the Elements of Style in Workflow creation approach as taught in the https://nih-nichd.github.io, the team will work together to containerize the processing steps and stitch them together in a workflow language.   On Cavatica, the workflow language best supported is Common Workflow Language (CWL).

## Background
[Background Slides](https://docs.google.com/presentation/d/1esjKl4iIlidfSdeqqJ7LwoOxeMA98vDa5TC5pmtq804/edit#slide=id.g2446d821512_0_0)

MYC is an oncoprotein and often implies worse outcomes, however it also seems to have a role in cardiovascular disease. Using open data from both the INCLUDE Data Hub and the Kids First Data Resource Portal, this Hackathon will:

* Explore MYC expression and its segregating effects at the intersection of congenital heart defects and cancer

* Build platform agnostic workflows and analysis notebooks using the elements of style method (https://nih-nichd.github.io) that will use both WGCNA and limma to probe the dual role of this gene.

* Result both in a tutorial of how to proceed from both https://portal.includedcc.org/ and https://portal.kidsfirstdrc.org to https://cavatica.sbgenomics.com/ as well as produce results in notebooks that could be used as figures in a paper promoting open transparent, reproducible results.

## Moving from Portal to Platform …

1. Makes a matrix of gene x sample -- in our case the KF RNA-seq workflow was run first.
2. Seperate the samples between high and low MYC expression
3. Run WGNCA analysis after deciding the binning (what are the "treatments") including High MYC and Low MYC – a template we will move into  a jupyter lab notebook https://bioinformaticsworkbook.org/tutorials/wgcna.html#gsc.tab=0) 
4. If outcome (death, etc) is available -- do we see a difference between the two types
5. What are the outcome differences between high and low MYC expression for the different heart morphologies
6. Run annotation analysis on the sub categories -- what are the GO and Pathways -- maybe run Reactome analysis -- on the different matrices

Analysis plan - WGCNA exists as an R program - convert to a notebook - break out the DESeq from the WGCNA
* Treatment in the WGCNA sense is the condition of the sample:
* Trisomy and Disomy samples
* High Myc and Low Myc expression.  
* Birth defect (cardiac) and Blood Cancers
* Birth Defect (cardiac) and Solid Tumors

