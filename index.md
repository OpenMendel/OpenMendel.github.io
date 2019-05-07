## OpenMendel Project

OpenMendel is an open source project implemented in the [Julia](http://julialang.org) programming language that comprises a set of packages for statistical analysis to solve a variety of genetic problems. OpenMendel is the open source version of [Mendel](http://www.genetics.ucla.edu/software/mendel), a comprehensive package for exact statistical genetic analysis of qualitative and quantitative traits. OpenMendel currently provides the analysis options listed below, with additional options under development. Each analysis option is a separate Julia package. We invite the genetics community to contribute to the OpenMendel Project..

### Analysis Options:

* [AIM Selection](https://openmendel.github.io/MendelAimSelection.jl) selects the SNPs that are most informative at predicting ancestry for your data — the best Ancestry Informative Markers (AIMs). [Package name: MendelAimSelection.]
* [Estimate Frequencies](https://openmendel.github.io/MendelEstimateFrequencies.jl) calculates a likelihood-based estimate of allele frequencies. [Package name: MendelEstimateFrequencies.]
* [Gamete Competition](https://openmendel.github.io/MendelGameteCompetition.jl) implements a gamete competition analysis, which is a generalization of the TDT analysis. [Package name: MendelGameteCompetition.]
* [Gene Dropping](https://openmendel.github.io/MendelGeneDropping.jl) performs gene dropping with several useful options for the output. [Package name: MendelGeneDropping.]
* [Genetic Counseling](https://openmendel.github.io/MendelGeneticCounseling.jl)  performs risk calculations for genetic counseling problems. [Package name: MendelGeneticCounseling.]
* [GWAS](https://openmendel.github.io/MendelGWAS.jl) performs standard Genome-wide Association Studies. [Package name: MendelGWAS.]
* [Kinship](https://openmendel.github.io/MendelKinship.jl) computes kinship and other identity coefficients. [Package name: MendelKinship.]
* [Location Scores](https://openmendel.github.io/MendelLocationScores.jl) maps a trait via the method of Location Scores, i.e., multipoint linkage analysis. [Package name: MendelLocationScores.]
* [Two Point Linkage](https://openmendel.github.io/MendelTwoPointLinkage.jl) performs two-point linkage analysis. [Package name: MendelTwoPointLinkage.]

### Utilities

OpenMendel also includes the following utility packages:

* [MendelBase](https://openmendel.github.io/MendelBase.jl) contains the base functions of OpenMendel.
* [MendelSearch](https://openmendel.github.io/MendelSearch.jl) is a program for function optimization. Search permits bounds and linear constraints to be imposed on parameters and, in statistical applications, computes asymptotic standard errors and correlations of parameter estimates.
* [SnpArrays](https://openmendel.github.io/SnpArrays.jl/latest/) provides utilities for handling compressed storage of biallelic SNP data.
* [VarianceComponentModels](https://openmendel.github.io/VarianceComponentModels.jl/latest/) provides utilities for fitting and testing variance components models, also known as linear mixed models.

### Installation

*Note: The three OpenMendel packages (1) [SnpArrays](https://openmendel.github.io/SnpArrays.jl/latest/), (2) [MendelSearch](https://openmendel.github.io/MendelSearch.jl), and (3) [MendelBase](https://openmendel.github.io/MendelBase.jl) must be installed before any other OpenMendel package will run. It is easiest if these three packages are installed in the above order and before any other OpenMendel package.*

Within Julia, use the package manager to install an OpenMendel package, for example, to install MendelBase, use the command:

    pkg> add https://github.com/OpenMendel/MendelBase.jl.git

All OpenMendel packages support Julia v1.0+.

### Data Files

To run an analysis package you will need to prepare a Control file and have your data files available. The Control file holds your data filenames and any optional parameters for the analysis. Details on the format and contents of the Control and data files can be found in the [MendelBase documentation page](https://openmendel.github.io/MendelBase.jl). Descriptions of the relevant parameters (*keywords*) available within each analysis package are in its documentation page (see the links above).

There are example data files in the "data" subfolder of each Mendel package.

### Running the Analysis

To run an analysis package, first launch Julia. Then load the package, for example MendelGWAS, with the command:

     julia> using MendelGWAS

Next, if necessary, change to the directory containing your files, for example,

     julia> cd("~/path/to/data/files/")

Finally, to run the analysis using the parameters in your Control file, for example, Control_file.txt, use the command:

     julia> GWAS("Control_file.txt")

*Note: Mendel analysis packages are named with the Mendel prefix, for example,* MendelGWAS, *but the actual analysis functions do not have the prefix, for example,* GWAS.

### Citation

If you use this analysis package in your research, please cite the following reference in resulting publications:

*Zhou H, Sinsheimer JS, Bates DM, Chu BB, German CA, Ji SS, Keys KL, Kim J, Ko S, Mosher GD, Papp JC, Sobel EM, Zhai J, Zhou JJ, Lange K.*

### Acknowledgments

This project is supported by the National Institutes of Health under NIGMS awards R01GM053275 and R25GM103774 and NHGRI award R01HG006139.
