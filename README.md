# GenePredictionBenchmarking
This repository contains the code for benchmarking three popular prokaryotic gene prediction tools – Prodigal, FragGeneScan, and AUGUSTUS – across ten archaeal genomes of varying GC contents.

# Background
Gene prediction, the process of identifying regions of DNA that encode proteins, is an essential step in understanding an organism after it has been sequenced. Once dependent on experimental testing alone, currently, there are many computational gene prediction tools available, ranging in capability for prokaryotes and eukaryotes. Most work by identifying essential structural elements and motifs of a genome to build predictive functionality, though not all are created equally or tested robustly. With the expansion of archaeal genome prominence from environmental and metagenomic studies, reliably predicting their coding sequence becomes more important to accurately annotate their genomes. This study aims to address the gap in knowledge for archaea species by benchmarking three popular prokaryotic gene prediction tools – Prodigal, FragGeneScan, and AUGUSTUS – across ten archaeal genomes of varying GC contents. We found that Prodigal was the top performer across nearly all metrics, achieving the highest composite score, individual metric rankings, and best overall scaling in regard to both runtime and memory usage. AUGUSTUS was second best when used with an appropriate model, and FragGeneScan, while fast, was computationally expensive and resulted in a high false positive rate. By identifying which tools perform most reliably on archaeal genomes, this benchmarking study demonstrates how tool selection directly affects prediction quality and reinforces the importance of choosing the most accurate methods to support downstream analyses.

# Python Notebook (Running Tools)
The Python notebook in this repository outlines in detail the code used to download the genomes and annotation files, parse ground truth, run and parse output for AUGUSTUS using bacteria and archaea models, run Prodigal, run FragGeneScan, and run GFFCompare for all tests. As there are 10 genomes tested for each tool, the code streamlines the process by looping through and running the commands, and making sure the output is place in the appropraite folder. 
* [Python Notebook](https://github.com/richapatel138/GenePredictionBenchmarking/blob/main/BenchmarkingProject_Python.ipynb)
* [Python HTML File](https://github.com/richapatel138/GenePredictionBenchmarking/blob/main/BenchmarkingProject_Python.html)

# R Markdown (Analysis)
The R makrdown file in this repository outlines the code used to generate tables and plots for analysis. It uses the manually curated ComparisonStats.csv, which is also included in this repository. 
* [Comparisons CSV](https://github.com/richapatel138/GenePredictionBenchmarking/blob/main/ComparisonStats.csv)
* [R Markdown](https://github.com/richapatel138/GenePredictionBenchmarking/blob/main/BenchmarkingProject_R.Rmd)
* [R HTML File](https://github.com/richapatel138/GenePredictionBenchmarking/blob/main/BenchmarkingProject_R.html)

