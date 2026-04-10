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
Repository for all data and code associated with paper exploring 24 hour urine reference ranges using data derived from systematic review and meta-analysis. 
<br>

These analyses are deployed online at: https://endourology.shinyapps.io/24_hr_ranges/. The app has three components: <br>
1. A patient report generation section, which the user can use to input values and generate a report comparing our systematic review/meta-analysis derived expected ranges compared to existing reference ranges.
2. A Main Results section, simply showing the main results from this study.
3. An exploratory section, where users can explore all the analyses performed within this study
<br>

## 2. How to Run this Analysis
<br>

**To download this model, open your terminal and use:**
```git clone https://github.com/rg2u17/24_hour_urine.git```
<br>
This will clone this repository into the working directory you are currently located in - for first time users of the terminal this will be your main folder (containing all files on your computer). We suggest setting your working directory to somewhere more helpful such as the Desktop or Documents folder. Do this before cloning the repository:
```cd .../Desktop``` NB ... should be replaced with the file path to your Desktop.
<br>
If you haven't already done so, we would suggest downloading RStudio from: https://posit.co/products/open-source/rstudio/?sid=1
Once RStudio is installed and you've downloaded the repository you will need to load in the rmarkdown file as below:
<br>

**To run this script we suggest using the rmarkdown file (Main 24hr urine MA for paper.rmd) in RStudio and either:** <br>
1. **selecting 'run all' OR** <br>
2. **knit the file to html** (NB: This markdown document is designed to be knitted to html, however we understand that readers may wish to adjust the script themselves) <br>
<br>

Prior to running the script please check all packages are installed - if not, then you can run this in the console prior to running all the markdown chunks: <br>
```install.packages(c("tidyverse", "gt", "gtExtra", "shiny", "data.table", "janitor", "pROC", "ggplot2", "janitor","DataExplorer","meta","metafor","forestplot","grid","gridExtra,"patchwork"))``` <br>
<br>

**File paths:**
There are no additional scripts that need to be run for this markdown document<br>
```getwd()``` <br>
<br>
The output should be: <br>
<br>
```.../24_hour_urine``` <br>
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
Figure 1. PRISMA Flow diagram <br>
<br>
### 3.2 Meta-analysis
We generated meta-analysed expected ranges based on the assumption of normal distribution, apart from volume where we assumed a left-skew and therefore performed a log transformation. The expected range was calculated according to existing standards for reporting reference ranges (<5% / >95% for normal distribution). A random-effects model was used when substantial heterogeneity was suspected, while a fixed-effect model was applied when there was minimal heterogeneity. Heterogeneity was evaluated using I2, τ2, and Cochran’s Q statistics. Publication bias was assessed statistically with Egger’s and Begg’s tests, and visually with Funnel/Baujat plots. 

We performed sub-analyses for age, sex, race, and sensitivity analyses for study design (RCT only) and risk of bias (low only and low/moderate only). We tested differences between sub-analyses with Wald tests.

Where there was sufficient data, we performed meta-regression using age, sex, race, study size and overall risk of bias as covariates. 

<br>
<img width="760" height="320" alt="image" src="https://github.com/user-attachments/files/24741908/MA.result.flow.diagram.pdf" /> <br>
Figure 2. Flow diagram of Workflow for meta-analysis
<br>
### 3.3 Bias analysis
We utilized the Cochrane risk of bias tools for both observational studies (exposures)10 and randomized trials. We summarized bias into an overall category. This was based on: any domain being high risk then overall was assigned high risk; if any two domains were moderate then overall was assigned moderate; otherwise overall was assigned to low risk. 
<br>
### 3.4 GRADE rating
We utilized the GRADE methodology to determine level of evidence for each of meta-analysis derived 24-hour urine reference range.
Please see: https://www.gradepro.org 

