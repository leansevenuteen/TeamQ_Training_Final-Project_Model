# TeamQ_ModelB
## What is this repository about? 
The model was built with the idea of available reports in order to classify security vulnerabilities. The data source is [NVD - National Vulnerability Dataset](https://nvd.nist.gov/)

## Quick Start
Clone this repository, configure a suitable Python 3 and Jupyter Notebook environment.
```bash
git clone https://github.com/leansevenuteen/TeamQ_Training_Final-Project_Model.git
cd TeamQ_Training_Final-Project_Model
```
Before running the code, you'll need to fetch the data by running `NVDDataFetch.ipynb`.

## Overview
After running `NVDDataFetch.ipynb`, you'll have `combined_data.csv` in the `./src` folder. This csv file contains vulnerabilities with their reports and their classification into 13 labels which are: 
- memcached
- bypass 
- cross site request forgery
- directory traversal
- denial of service 
- execution
- file inclusion
- gain privilege
- http response splitting
- information disclosure
- overflow
- sql injection 
- cross site scripting


The `./src/cveIDThreatType/` folders contains bunchs of `txt` file which classified vulnerabilities. One vulnerability can be classified into 1 or more labels.

The `./src/vulner_embedding.bin` is a pretrained model in another github called [Vul_Word2Vec](https://github.com/unsw-cse-soc/Vul_Word2Vec). This pretrained model is used for words embedding in the `report` column into float numbers for training ML models. 
