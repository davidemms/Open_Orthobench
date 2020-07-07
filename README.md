# Orthobench Revisited
This is the GitHub repository for a complete reanalysis of the Orthobench benchmarks for orthogroup inference accuracy. It contains 70 currated bilaterian orthogroups based on the orthogroups from the original Orthobench study: 

Trachana, K., Larsson, T.A., Powell, S., Chen, W.‐H., Doerks, T., Muller, J. and Bork, P. (2011), Orthology prediction methods: A quality assessment using curated protein families. Bioessays, 33: 769-780. [doi:10.1002/bies.201100062](https://doi.org/10.1002/bies.201100062)

There have been a number of major corrections to the currated orthogroups, which together improve the accuracy of the benchmarks considerably. The paper reporting this reanalysis will be submitted for peer review. The updated orthogroups together with the complete set of data supporting the analysis are provided in this repository. The issues page is open, so anyone can identify any further corrections that are required and can submit the data supporting the correction.

# Citation
Please cite the original Orthobench paper above (Trachana et al.) and this GitHub repository. An updated citation in place of the GitHub repository will be provided once it is available. 

# Description of Files

There are two main directories
* **BENCHMARKS**: Contains all the files you need to benchmark an orthogroup inference method.
* **Supporting_Data**: Contains all the data supporting the curration of the 70 bilaterian orthogroups (RefOGs). If you want to critique the curration of the orthogroups that form the benchmark then these files explain the reasoning behind the exclusion/inclusion of genes in each RefOG.

The contents of this directory are as follows.

## BENCHMARKS - data & script for benchmarking orhtogroup infernece methods
* Input - the 12 input proteomes for the orthogroup inference method to be tested
* RefOGs - the genes in each RefOG as determined by this study
* benchmark.py - python script to calculate the benchmarks for a user-supplied set of inferred orthogroups

## Supporting_Data - Data supporting the inferred RefOGs
This contains two subdirectories 
	
### Data_for_RefOGs - The data associated with the inference of each RefOG
* sequences - the sets of sequences used for tree inference
* alignments - the MSA for each sequence file
* trees - the trees inferred from the MSAs
* trees\_tight - a tree for each RefOG cropped tightly around the RefOG
* evidence - the evidence considered for each RefOG in determining which genes belong to each RefOG
* low\_certainty_assignments - those genes that have been included/excluded from a RefOG but for which this could only be done with low certainty

### Additional_Files
* proteomes - the proteomes for the 12 study species plus additional in-group and out-group species used to help determine the gene membership for each RefOG
* original\_study\_trees - gene trees from the original study
* hmm\_profiles - hmm profiles from the original study for the RefOGs
* hmmer\_results - HMMER results for searching the hmm profiles against the proteomes used for this study
* additional\_identified\_orthogroups - Additionally identified orthogroups determined in the process of determining the membership of the target orthogroups
