# Exploration of 24 Hour Urine References Ranges Using SR/MA data
## Table of Contents
<br>

| Item                                      | Section |
| ----------------------------------------- | ------: |
| [Explanation](#1-explanation) | 1 |
| [How to Run this Analysis](#2-how-to-run-this-analysis) | 2 |
| [Workflow](#3-workflow) | 3 |


<br>

## 1. Explanation
Repository for all data and code associated with paper exploring 24 hour urine reference ranges using data derived from systematic review and meta-analysis
<br>
## 2. How to Run this Analysis
**To run this script we suggest using the rmarkdown file (Main 24hr urine MA for paper.rmd) in RStudio and either: selecting 'run all' or knit the file to html** <br>
<br>
This markdown document is designed to be knitted to html, however we understand that readers may wish to adjust the script themselves. <br>
Prior to running the script please check all packages are installed - if not, then you can run this in the console prior to running all the markdown chunks: <br>
```install.packages(c("tidyverse", "gt", "gtExtra", "DiagrammeR", "data.table", "janitor", "pROC", "ggplot2", "pracma", "glue", "cutpointr", "caret", "cowplot", "ggsignif", "ggpubr", "broom", "pryr", "lubridate", "sfsmisc", "patchwork", "mice", "furrr","purrr","future","boot"))``` <br>
<br>
**File paths:**
There are no additional scripts that need to be run for this markdown document<br>
```getwd()``` <br>
<br>
The output should be: <br>
<br>
.../24_hour_urine <br>
<br>
Otherwise you will need to assign the working directory to where the file is stored, for example:
<br>
```setwd('~/Desktop/24_hour_urine')``` <br>
<br>
To set the working working directory to an appropriate place <br>
This will ensure the scripts run without having to alter the file path

## 3. Workflow
We utilised the following workflow:
<br>
### 3.1 Systematic review 
Explanation re: SR
<br>
All the documents identified in the original search are within the Searches Folder as .docx files ('24 hour urine and kidney stones.docx' and '24 hour urine and stones - part 2.docx')
<br>
### 3.2 Meta-analysis
Explanation re: MA
<br>
<img width="760" height="320" alt="image" src="https://github.com/user-attachments/files/24741908/MA.result.flow.diagram.pdf" /> <br>
Figure 2. Flow diagram of Workflow for meta-analysis
<br>
### 3.3 Bias analysis
Explanation re: bias analysis <br>
<br>
### 3.4 GRADE rating
Explanation re: GRADE <br>
<br>

### 3.5 Clinical Cohort Testing
Explanation re: clinical testing
<br>

