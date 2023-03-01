# Welcome to the Heinig lab

## Overview

The [Heinig lab](https://www.helmholtz-munich.de/en/research-group-lab-40-2) is located at the [Insitiute of Computational Biology](https://comp.bio), which is part of the [Computational Health Center](https://www.helmholtz-munich.de/computational-health-center/) of [Helmholtz Munich](https://www.helmholtz-munich.de/).

Together with my research group, I develop **AI solutions for personalized network based precision medicine**.

Technological advances allow for an unprecedented in-depth characterization of the molecular basis of complex diseases. In particular SNP genotyping, DNA methylation assays and gene expression profiling in large cohorts have been used to identify numerous disease associated loci and genes. However, a deeper mechanistic or systems level understanding of disease processes still remains elusive in most cases.

The aim of our research is the development and application of computational and statistical tools for the identification of molecular regulatory networks underlying common diseases and the genetic and epigenetic mechanisms controlling these networks from population level DNA and multi-omics data sets. In a second step we aim to personalize the networks based on single cell data. This will enable us to implement new concepts for precision medicine. A special focus is the molecular characterization of metabolic and cardiovascular diseases, in particular diabetes and arrhythmias like atrial or ventricular fibrillation.

![Using regulatory networks to understand complex traits](img/group_scheme_crop.png)

## Projects

### Using natural genetic and epigenetic variation to characterize regulatory networks underlying complex diseases

Motivated by the fact that most disease associated variants identified to date are located in non-coding parts of the genome, which likely harbors regulatory elements, we are studying the effect of naturally occurring sequence variation on gene regulation. To characterize regulatory sequence variants two related challenges have to be met: 1) regulatory elements have to be recognized and 2) the corresponding target genes have to be identified. Epigenetic marks such as histone modifications have proved instrumental for the identification of regulatory elements in the genome, while the integrated analysis of genetic variation and gene expression provides a strategy (expression QTL mapping) to identify targets of regulatory variants. Ultimately the integration of genetic, genomic and epigenomic data set is expected to lead to a comprehensive understanding of regulatory sequence variation and its role in disease. Towards these goals we have:

- developed a random walk approach to identify the regulatory networks underlying common disease from DNA-methylation data [(Hawe Nature Genetics 2022)](https://www.nature.com/articles/s41588-021-00969-x) - [code](https://github.com/heiniglab/hawe2021_meQTL_analyses#identification-of-eqtms)
- extended this approach using Bayesian graphical models to make full use of prior networks and the correlation structure in the data [(Hawe Genome Medicine 2022)](https://genomemedicine.biomedcentral.com/articles/10.1186/s13073-022-01124-9) - [code](https://github.com/jhawe/bggm/)
- integrated proteomics and gene expression to identify cis and trans acting eQTL/pQTL in the human atrial appendage [(Assum Nature Communications 2022)](https://www.nature.com/articles/s41467-022-27953-1) - [code](https://github.com/heiniglab/symatrial) 
- reviewed current methods for network reconstruction from multi-omics data [(Hawe Frontiers in Genetics 2019)](https://www.frontiersin.org/articles/10.3389/fgene.2019.00535/full)
- performed one of the largest eQTL studies to date in the human heart [(Heinig Genome Biology 2017)](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-017-1286-z)
- developed the computational tool [histoneHMM](https://github.com/matthiasheinig/histoneHMM) for the identification of differentially modified regions for histone modifications with broad genomic footprints [(Heinig BMC Bioinformatics 2015)](https://pubmed.ncbi.nlm.nih.gov/25884684/)
- developed predictive models to identify functional genomic elements predictive of regulatory variants [(Budach, Heinig* and Marsico* Genetics 2016)](https://academic.oup.com/genetics/article/203/4/1629/6065860)
- performed an integrated analysis of the consequences of genetic variation for multiple levels of epigenetic and transcriptional regulation [(Rintisch*, Heinig* Genome Res 2014)](https://pubmed.ncbi.nlm.nih.gov/24793478/)
- developed a statistical approach for the identification of a transcription factor driven regulatory network, including its master regulator and the interpretation of disease association (type 1 diabetes) using this regulatory network [(Heinig Nature 2010)](https://pubmed.ncbi.nlm.nih.gov/20827270/)
- developed the computational tool [sTRAP](http://trap.molgen.mpg.de/cgi-bin/home.cgi) for the identification of causative cis regulatory variants affecting transcription factor binding [(Manke*, Heinig* Hum Mutat 2010)](https://pubmed.ncbi.nlm.nih.gov/20127973/) and successfully applied this tool in a disease gene study [(Monti Nat Genet 2008)](https://pubmed.ncbi.nlm.nih.gov/18443590/) for heart failure


### Using single cell trancriptomics to personalize gene regulatory networks

Single cell RNA-seq not only enables us to explore the individual celltypes and their transcriptional programs. It also enables to study the effects of common and rare gene variation with celltype resolution. Importantly, it enables us to personalize gene regulatory networks. 

Current approaches infer a single network, which can be thought of as a static reference for the whole population. In reality however, inter-individual differences in the genome and the environment are expected to cause differences in the network topology. Therefore, not just a single reference core gene network but a personalizable core gene network is required for precision medicine applications. Single cell RNA-seq measures the full transcriptomes of multiple cells of the same person. This allows to infer person and celltype-specific gene regulatory networks.

To fully leverage the potential of single cell data we have:

- teamed up with the [seed network for the human cell atlas](https://chanzuckerberg.com/science/programs-resources/single-cell-biology/seednetworks/a-spatial-cell-type-reference-atlas-of-the-adult-human-heart/) to build the first reference cell atlas of the human heart [(Litvinukova Nature 2020)](https://www.nature.com/articles/s41586-020-2797-4) - [code](https://github.com/cartal/HCA_Heart)
- studied the effect of rare pathogenic variants on cardiac celltype composition and expression programs in patients with dilated cardiomyopathy [(Reichart  Science 2022)](https://www.science.org/doi/10.1126/science.abo1984) - [code](https://github.com/heiniglab/DCM_heart_cell_atlas)
- teamed up with the [single cell eQTLgen consortium](https://www.eqtlgen.org/sc/index.html) to outline a strategy to identify cell type specific eQTL [(van der Wijst Elife 2020)](https://elifesciences.org/articles/52155)
- developed [scPower](http://scpower.helmholtz-muenchen.de): the first scalabel and generally applicable power analysis tool for multi-sample single cell transcriptomics experiments such as eQTL [(Schmid Nature Communications 2021)](https://doi.org/10.1038/s41467-021-26779-7) - [code](https://github.com/heiniglab/scPower)
- developed computational approaches to personalize co-expression networks [(Li Genome Biology 2023 - in press)](https://www.biorxiv.org/content/10.1101/2022.04.20.488925v1)


### Identifying disease core genes and their networks

Complex traits are associated with houndreds if not thousands of non-coding variants throughout the whole genome. Theoretical models such as the [omnigenic core gene model](https://www.cell.com/cell/pdf/S0092-8674(19)30400-3.pdf) have been proposed to reconcile this observed genetic architecture with the potential molecular mechanisms: when small effects of multiple risk loci converge on the same downstream core genes in regulatory networks, a large proportion of the heritability can be explained. The key challenges are that downstream targets are difficult to identify using QTL data and that the core genes for specific diseases are unknown.

To adress these challenges, we have:

- developed [Speos](https://github.com/fratajcz/speos) - a graph neural network approach to predict core genes of complex disease from network, GWAS and gene expression data [(Ratajzcak bioRxiv 2023)](https://www.biorxiv.org/content/10.1101/2023.01.13.523556v1) - [code](https://github.com/fratajcz/speos) - [docs](https://speos.readthedocs.io/en/latest/index.html)
- developed a data integration approach that makes use of polygenic risk scores and pathway annotations to identify trans-acting QTL from protein and transcript expression data. We applied it to the atrial fibrillation cohort of the symAtrial consortium to identify candidate core genes of atrial fibrillation [(Assum Nature Communications 2022)](https://www.nature.com/articles/s41467-022-27953-1) - [code](https://github.com/heiniglab/symatrial) 

### Publications

[Visit google scholar](https://scholar.google.com/citations?user=Is48SCoAAAAJ&hl=en) for a full list of publications.

**Selected publications:**
1. Li S*, Schmid KT*, de Vries D*, Korshevniuk M, Oelen R, van Blokland I, BIOS Consortium, sc-eQTLgene Consortium, Groot HE, Swertz M, van der Harst P, Westra HJ, van der Wijst M, Heinig M†, Franke L†. [Identification of genetic variants that impact gene co-expression relationships using large-scale single-cell data](https://doi.org/10.1101/2022.04.20.488925). bioRxiv 2022; doi: https://doi.org/10.1101/2022.04.20.488925 (in press at Genome Biology)
1. Hawe JS*, Wilson R*, Schmid KT*, Zhou L, Lakshmanan LN, Lehne BC, Kühnel B, Scott WR, Wielscher M, Yew YW, Baumbach C, Lee DP, Marouli E, Bernard M, Pfeiffer L, Matías-García PR, Autio MI, Bourgeois S, Herder C, Karhunen V, Meitinger T, Prokisch H, Rathmann W, Roden M, Sebert S, Shin J, Strauch K, Zhang W, Tan WLW, Hauck SM, Merl-Pham J, Grallert H, Barbosa EGV; MuTHER Consortium, Illig T, Peters A, Paus T, Pausova Z, Deloukas P, Foo RSY, Jarvelin MR, Kooner JS, Loh M†, Heinig M†, Gieger C†, Waldenberger M†, Chambers JC†. [Genetic variation influencing DNA methylation provides insights into molecular mechanisms regulating genomic function](https://www.nature.com/articles/s41588-021-00969-x). Nat Genet. 2022;54(1):18-29
2. Schmid KT, Höllbacher B, Cruceanu C, Böttcher A, Lickert H, Binder EB, Theis FJ, Heinig M. [scPower accelerates and optimizes the design of multi-sample single cell transcriptomic studies](https://doi.org/10.1038/s41467-021-26779-7). Nat Commun. 2021 Nov 16;12(1):6625.
3. Assum I*, Krause J*, Scheinhardt MO, Müller C, Hammer E, Börschel CS, Völker U, Conradi L, Geelhoed B, Zeller T, Schnabel RB†, Heinig M†. [Tissue-specific multi-omics analysis of atrial fibrillation](https://www.nature.com/articles/s41467-022-27953-1). Nat Commun. 2022 Jan 21;13(1):441. 
4. Heinig M*, Petretto E*, Wallace C, Bottolo L, Rotival M, Lu H, Li Y, Sarwar R, Langley SR, Bauerfeind A, Hummel O, Lee YA, Paskas S, Rintisch C, Saar K, Cooper J, Buchan R, Gray EE, Cyster JG; Cardiogenics Consortium, Erdmann J, Hengstenberg C, Maouche S, Ouwehand WH, Rice CM, Samani NJ, Schunkert H, Goodall AH, Schulz H, Roider HG, Vingron M, Blankenberg S, Munzel T, Zeller T, Szymczak S, Ziegler A, Tiret L, Smyth DJ, Pravenec M, Aitman TJ, Cambien F, Clayton D, Todd JA, Hubner N, Cook SA. [A trans-acting locus regulates an anti-viral expression network and type 1 diabetes risk](https://pubmed.ncbi.nlm.nih.gov/20827270/). Nature. 2010; 467(7314):460-4 ‡
5. Litvinukova M, Talavera-Lopez C, Maatz H, Reichart D, Worth CL, Lindberg EL, Kanda M, Polanski K, Fasouli ES, Samari S, Roberts K, Tuck E, ​Heinig M​, DeLaughter D, McDonough B, Wakimoto H, Gorham JM, Nadelmann E, Mahbubani KT, Saeb-Parsy K, Patone G, Boyle JJ, Zhang H, Zhang H, Viveiros A, Oudit G, Bayraktar O, Seidman JG, Seidman C, Noseda M, Hubner N, Teichmann SA. [Cells and gene expression programs in the adult human heart](https://www.nature.com/articles/s41586-020-2797-4). Nature. 2020; 588;466 ‡
6. van der Wijst M, de Vries DH, Groot HE, Trynka G, Hon CC, Bonder MJ, Stegle O, Nawijn MC, Idaghdour Y, van der Harst P, Ye CJ, Powell J, Theis FJ, Mahfouz A, ​Heinig M​, Franke L. [The single-cell eQTLGen consortium](https://elifesciences.org/articles/52155). Elife. 2020;9:e52155
7. Manke T*, Heinig M*, and Vingron M. [Quantifying the effect of sequence variation on regulatory interactions](https://pubmed.ncbi.nlm.nih.gov/20127973/). Hum Mutat. 2010; 31(4):477-83  ‡
8. Budach S, Heinig M*, Marsico A*. [Principles of microRNA Regulation Revealed Through Modeling microRNA Expression Quantitative Trait Loci](https://academic.oup.com/genetics/article/203/4/1629/6065860). Genetics. 2016; pii: genetics.116.187153
9. Heinig M*, Adriaens ME*, Schafer S*, van Deutekom HWM, Lodder EM, Ware JS, Schneider V, Felkin LE, Creemers EE, Meder M, Katus HA, Rühle F, Stoll M, Cambien F, Villard E, Charron P, Varro A, Bishopric NH, George Jr. AL, dos Remedios C, Moreno Moral A, Pesce F, Bauerfeind A, Rüschendorf F, Rintisch C, Petretto E, Barton PJ, Cook SA, Pinto Y, Bezzina CR, Hubner N. [Natural genetic variation of the cardiac transcriptome in non-diseased donors and patients with dilated cardiomyopathy](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-017-1286-z). Genome Biology. 2017; 18(1);170 ‡
10. Rintisch C*, Heinig M*, Bauerfeind A, Schafer S, Mieth C, Patone G, Hummel O, Chen W, Cook S, Cuppen E, Colome-Tatche M, Johannes F, Jansen RC, Neil H, Werner M, Pravenec M, Vingron M, and Hubner N. [Natural variation of histone modification and its impact on gene expression in the rat genome](https://pubmed.ncbi.nlm.nih.gov/24793478/). Genome Res. 2014; 24(6):942-53 ‡

