# efaecium-niche
Code for reproducing e. faecium niche paper results.

## 0. Compute tools
External tools are available for the download and processing of our data.
##### Data downloader
Download [Dr. Finlay Maguire's](https://github.com/fmaguire) data aqcusition tool from [here.](https://github.com/fmaguire/enterococcus_sample_reconciliation)<br>
`git clone https://github.com/fmaguire/enterococcus_sample_reconciliation`

##### ARETE pipeline
A bulk of the data processing and analysis in this work can be replicated by running the ARETE Nextflow pipeline, a pipeline designed for end-to-end assembly and annotation of bacterial genomes. <br>
Download the code from [here:](https://github.com/beiko-lab/arete)
`git clone https://github.com/beiko-lab/arete`

##### BayesTraits
You will need to install the BayesTraits executable from (here)[http://www.evolution.rdg.ac.uk/].

##### IslandCompare
**TODO**

##### DBSCAN-SWA
**TODO** 

## 1. Download the data and metadata
`bash enterococcus_sample_reconciliation/genomes/download.sh` <br>
**todo: upload script that extracts faecium only, make into ARETE sample sheet**<br>
**todo: reference and outgroup genomes**

## 2. Run ARETE
`nextflow run arete/ --input_sample_table data/samplesheet.py --reference_genome data/Efaecium_DO.fasts --outgroup_genome data/ehirae.fasta`

## 3. Run data post-processing scripts
1. filter_sort_concat.py
2. crosstab
3. BayesTraits

## 4. Run IslandCompare and DBSCAN-SWA
**TODO**

## 5. Create figures and tables
Simply open the Figures.ipynb and Tables.ipynb and run them.

