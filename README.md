# IVAG
Integrative Visualization Application for various Genomic Data

## Introduction
IVAG is a user friendly web application for visualizing RNA-Seq and GWAS data.
It is designed for non-computer based scientists to explore there processed data interactively
just by a simple click.
IVAG is developed in R using shiny package and is dockerized with all required dependencies
to avoid compatibility issue.

## Functions

### RNA-Seq
- Differentially expressed Gene analysis
- Visualization
  - Heatmap
  - Volcano plot
  - PCA plot
- Gene Ontology Enrichment analysis

### GWAS
- LD analysis
- Gene ID annotation
- Visualization
  - Manhattan plot
  - QQ plot
  - LD heatmap
  
### Genome Browser
- Genome Browser build
- Various track creation
- Interactive visualization of RNA-Seq and GWAS data

## Installation
### Window
1. Download ivag.v1.tar file.
2. Open CMD and change directory where ivag.v1.tar file is downloaded.
3. Type following on CMD: ``` docker load -i ivag.v1.tar ```
4. Type following on CMD:
   ```
   docker run -ti -v YOUR_LOCAL_DIRECTORY_TO_MOUNT:/jbrowse/my_data -p 8080:80 -p 8383:3838 leetaerim/ivag:v1 /bin/bash -c "Rscript load.R"
   ```
   - Make sure that your local directory to mount consists of a subdirectory called raw, json and plink
   - When you want to share this web-interface with your team, add ``` -e HOST_IP='YOUR_IP_ADDRESS' ``` to docker run command
5. Start the app by typing fowiing URL into your internet browser.
    - IVAG - RNAseq, GWAS, JBrowse : localhost:8383
    - IVAG - JBrowse : localhost:8080
    
    The construction of the genome browser should be done at localhost:8383
    when you typing this URL, you can type localhost IP instead of localhost.

## Detailed manual can be downloaded in PDF format.
