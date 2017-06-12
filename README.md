# Mental health outcomes data harmonization work repository
Welcome to the *Mental health outcomes domain* data harmonization work repository! Documenation of DataSchema variables as well as versionning and storage of data harmonization scripts will be saved in this space. 

This page includes information to get you started.

## Table of Contents
1. [Introduction to RMarkdown](#introduction-to-rmarkdown) 
2. [DataSchema variable template](#dataschema-variable-template)
3. [DataSchema variable example](#dataschema-variable-example)
4. [R scripts](#r-scripts)

 
## Introduction to RMarkdown
An R Markdown document will be used to define the DataSchema (i.e. variables targeted for harmonization) covering each domain of information targeted by MINDMAP and to write R scripts used to derive common-format (i.e. harmonized) data. **RMarkdown** is essentially a file which encorporate **Markdown** - a lightweight markup language with plain text formatting syntax, and **R** - an open source programming language and software environment for statistical computing.

Markdown will be used to document DataSchema variable metadata (e.g. variable labels, descriptions, units, coding for categories) and R scripts will be used to harmonize data. That is, once completed, the RMarkdown file will contain the metadata which describes harmonized variables (in Markdown format) as well the data harmonization scripts that were used to generate common format data (in R language).

For more details on using RMarkdown see <http://rmarkdown.rstudio.com>. The following links will also help you get familiar with R Markdown:
 - <http://www.rstudio.com/wp-content/uploads/2015/03/rmarkdown-reference.pdf>
 - <http://www.rstudio.com/wp-content/uploads/2016/03/rmarkdown-cheatsheet-2.0.pdf>
 

## **DataSchema variable template**  
To begin, each lead harmonizer will need to define DataSchema variables for the domain they were attributed. All fields which should be documented are outlined in the template below. Each MINDMAP harmonization lead will need to fill out this template for each DataSchema variable they define. Since study-specific data will then be mapped to these variables, it is important to give as much detail as possible in the **Variable description** field.

Documentation of DataSchema variable metadata should be done using the following template:

### **Variable label** -  a short label describing what the variable measures  
**Variable name** -  a computer-readable name (variable naming guidelines to follow)  
**Variable description**  - a detailed description of the variable, which might include components such as whether the variable needs to be measured or self-reported, the recall period (current, in the past month, year), or the accepted information source (questionnaire or registries)  
**Value type** - integer, decimal, date, datetime, or text   
**Variable unit** - if applicable - e.g. cm, kg, mmol. If not applicable, leave blank   
**Category coding** - if applicable fill out table below with correct values. If not applicable (i.e. a continuous variable) delete the table.  

**Code** | **Category Label**  
------------- | -------------
0 | 
1 | 

**Harmonization status** - complete or impossible  
**Harmonization comment** - if needed, note on methodology or any reference used in the harmonization process  
**R script**  
```{r, echo=TRUE}
#This is where the R-script will be written

```

****
## **DataSchema variable example**

This is what the filled out template would look like for the *Cigarette smoking status* variable
  
### **Variable label**: Cigarette smoking status  
**Variable name**: lsb_smk_status  
**Variable description**: indicator of whether the participant is never, past, or current smoker. This variable targets cigarette smoking behaviour only and excludes cigar, pipes and other tobaco products  
**Value type**: integer  
**Variable unit**: N/A  
**Category coding**:  

**Code** | **Category Label**  
------------- | -------------  
0 | Never smoked  
1 | Past smoker  
2 | Current smoker  

**Harmonization status**: complete  
**Harmonization comment**: N/A  
**R script**:  
```{r, echo=TRUE}
#This is where the R-script will be written

```
***

## R scripts

As you see in the template above, Dataschema variable metadata are followed by R code chunks (the section below **R scripts:**), where data harmonization script will be written. R code chunks are created by three back ticks followed by an r in braces. They end with three back ticks.

Rscripts will be written in RStudio (details to follow).

