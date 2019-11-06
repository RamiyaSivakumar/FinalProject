# FinalProject
***
## Deliverables: 

The final deliverable that this project aims to compute is the log2(fold-change) plot of the gene expression of two subsets of brain cancer. The log2(fold change) is the logarithmic ratio of a gene’s expression under two different conditions under normalized conditions. In this particular case, the ratio of a gene’s expression under the two categories of age of diagnosis (1-30 (young) versus 30+(old)) will be analyzed. Multiple sub-deliverables will be met along the course of the experiment to verify the validity of the computation (e.g. logCountsPerMillion, which measures expression level).

![alt text](https://github.com/RamiyaSivakumar/FinalProject/blob/master/Project%20Outline%20Image.png)
***
## Datasets: 

The datasets that are taken for this study have been filtered from The Cancer Genomic Atlas Database. 

The filtered applied to choose a particular file are: 

Type of Cancer: Brain Cancer →Parameter Being Analyzed: Age of Diagnosis →Experimental Strategy: RNA Seq Data → Workflow Model: HTSeq- Counts

The files are of type: HTSeq- Counts

 HTSeq-Count files are presented in a tab-delimited format. The first column is the Ensemble gene ID and the second column denotes the number of mapped reads. The files do not contain a header, thus information of the first gene would be present on line one. 

There are about 200 available files under this criteria for each age category. The first 50 are chosen from the list. 

Upon loading the dataset, a unit test would be to print the first 10 lines of the file and the value returned would look similar to this:

![alt text](https://github.com/RamiyaSivakumar/FinalProject/blob/master/HTSeq-Counts%20Image.png)
***
## URL: 

Ages 1-30: 

https://portal.gdc.cancer.gov/repository?filters=%7B%22op%22%3A%22and%22%2C%22content%22%3A%5B%7B%22content%22%3A%7B%22field%22%3A%22cases.case_id%22%2C%22value%22%3A%5B%22set_id%3AAW46SnsFayU0iNGX1VgU%22%5D%7D%2C%22op%22%3A%22IN%22%7D%2C%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22files.analysis.workflow_type%22%2C%22value%22%3A%5B%22HTSeq%20-%20Counts%22%5D%7D%7D%2C%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22files.experimental_strategy%22%2C%22value%22%3A%5B%22RNA-Seq%22%5D%7D%7D%5D%7D

Ages 31+: 

https://portal.gdc.cancer.gov/repository?filters=%7B%22op%22%3A%22and%22%2C%22content%22%3A%5B%7B%22content%22%3A%7B%22field%22%3A%22cases.case_id%22%2C%22value%22%3A%5B%22set_id%3AAW46nqA44w3XaiNx32eS%22%5D%7D%2C%22op%22%3A%22IN%22%7D%2C%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22files.analysis.workflow_type%22%2C%22value%22%3A%5B%22HTSeq%20-%20Counts%22%5D%7D%7D%2C%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22files.experimental_strategy%22%2C%22value%22%3A%5B%22RNA-Seq%22%5D%7D%7D%5D%7D
***
## Proposed Analysis: 

The analysis that is to be conducted will utilize the libraries: 
	library(limma)
	library(glimma)
	library(edgeR)

These libraries specialize in working with RNASeq data. The edgeR package will be utilized in the importing, organization, filtering and normalization of the data. The limma package will assess the differential expression and test the gene sets. The Glimma package will enable the interactive exploration of the results and aid in the development of a User Interphase. 
***
## Proposed Timelines and Major Milestones: 

![alt text](https://github.com/RamiyaSivakumar/FinalProject/blob/master/Milestones.png)

## Proposed User Interface 
![alt text](https://github.com/RamiyaSivakumar/FinalProject/blob/master/Wire%20Diagram.png)


