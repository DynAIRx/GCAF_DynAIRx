# GCAF_DynAIRx

# Introduction
This repository is designed for Generalised Codelist Automation Framework (GCAF). It is part of DynAIRx Project (NIHR funded). It consist of multiple Python Jupyter Notebooks that perform specific tasks of modules of GCAF shown Figure below:

<!-- mapping files and utlity functions for conversion, grouping, and preparation of training data. Baseline database may consist of SNOMED, cvt codes, read codes, conditions/terms, descriptions etc.

This is framework created by Asra for Codelist Paper -->

![Generalised Codelist Automation Framework (GCAF)](/others/GCAF_Framework.png)




# Requirements
- Python (for development). If you dont have Python, you can install using https://www.python.org/downloads/ 
- Jupyter Notebook (for practice / run directly)

# How do I run these scripts?
- Run Jupyter Notebooks directly for conversions (For example CVT_to_SNOMED). You will be able to see results (expected) of each cell just by clicking on Run button

# Modules
- <b>`GCAF_Preprocessing.ipynb` </b>
This file is performas task of module GCAF Preprocessing. It is performing ReadCode to SNOMED for baseline-1 codelist.

- <b>`GCAF_Derive_Definite_Conditions.ipynb` </b>
This file is performas task of module GCAF Derive Definite Conditions. The purpose of this module is to scan all input codelist, perform text operations on condition names, and generate a list of definitive conditions. 

- <b>`Clincians_Intervention_Split_Keep_Group.xlsx` </b>
This file is for module Clinical Intervention. Tis fiel consist of guidance comments on which clinical concepts in the codelist need to be split and which to be grouped or merged based on the specific usecase of the project.

- <b>`GCAF_codelist_Distribution.ipynb` </b>
This file is performas task of module GCAF Codelists Distribution. On the basis of the clinicians' comments, this module distribute conditions into different types: keep comments type and Group/Split type comments.

- <b>About `GCAF_Investigate_Related_Condition_Names.ipynb` </b>
This file is performas task of module Investigate related condition names. This module focuss on concepts where the clinical team indicated the need for merging or splitting to produce a potential list of concepts we need to capture.

- <b>About `GCAF_Keywords_based_Codelist_Generation.ipynb` </b>
This file is performas task of module GCAF Keywords based Codelist Generation. This automated phase performs a keyword search across the preprocessed codelists (using terms from the previous step), fetching the associated SNOMED codes, and generating draft codelists for condition names agreed in the previous module. 


- <b>About `GCAF_Codelist_Comparison_for_Load_Reduction.ipynb` </b>
This file is performas task of module GCAF Codelist Comparison for Load Reduction. This module automatically validate codes using a trusted source (CALIBER for DynAIRx) and reduce loads for clinicans for reducing need to validate all codes. I produce Fully shrunk or partially shrunk codelists to validate.


- Please note Modules Grouping/Splitting of Codelists, Clinician’s Validation of Partially Shrunken codelists, and Clinician’s Validation of Partially Shrunken codelists are manual, detailed in paper.


# Useful Files
- <b>About `Multimorbidity_Codelist_16.11.2021.xlsx`</b>
    Mapping file for ReadCode to SNOMED used in abaseline codelists. Mapping file downloaded by Asra using website `NHS Data Migration - TRUD (digital.nhs.uk)`


- <b>About `Baseline1_Codelist.csv`</b>
    The LW codelists are from previous CPRD-based projects at Liverpool (details TBC). These appear to be in CTV3 (aka Read Code v3) format so they gets translated to SNOMED using a mapping file avaliable on the NHS TRUD website.

- <b>About `Baseline2_Codelist.csv`</b>
    The eFI refers to the electronic Frailty Index - a very successful clinical tool that has been deployed in all major GP systems. Sam Relton and Andy Clegg are currently finishing off the eFI2 project which expands upon this initial work to build prediction models. The SNOMED codes here are the basis of that work, used to define 80 long-term conditions that are used to predict mortality, hospitalisation with a fall, requirement for a homecare package, and nursing home admission (all measured as binary outcomes within the next 12 months).


## Citation

If you use this work in your research or project, please cite the following paper:

Aslam, A., Walker, L., Abaho, M., Cant, H., O'Connell, M., Abuzour, A. S., Hama, L., Schofield, P., Mair, F.S., Ruddle, R.A., Popoola, O., Sperrin, M., Tsang, J.Y., Shantsila, E., Gabbay, M., Clegg, A., Woodall, A.A., Buchan, I., & Relton, S. D. (2024). *An Automation Framework for Clinical Codelist Development Validated with UK Data from Patients with Multiple Long-term Conditions*. **medRxiv**. [https://doi.org/10.1101/2024.09.25.24314215](https://doi.org/10.1101/2024.09.25.24314215)

You can access the full paper [here](https://www.medrxiv.org/content/early/2024/09/26/2024.09.25.24314215.full.pdf).

### BibTeX Code for Paper in Latex

@article {Aslam2024.09.25.24314215, <br>
	author = {Aslam, A. and Walker, L. and Abaho, M. and Cant, H. and O Connell, M. and Abuzour, A. S. and Hama, L. and Schofield, P. and Mair, F.S. and Ruddle, R.A. and Popoola, O. and Sperrin, M. and Tsang, J.Y. and Shantsila, E. and Gabbay, M. and Clegg, A. and Woodall, A.A. and Buchan, I. and Relton, S. D.},<br>
	title = {An Automation Framework for Clinical Codelist Development Validated with UK Data from Patients with Multiple Long-term Conditions}, <br>
	elocation-id = {2024.09.25.24314215}, <br>
	year = {2024}, <br>
	doi = {10.1101/2024.09.25.24314215}, <br>
	publisher = {Cold Spring Harbor Laboratory Press}, <br>
	URL = {https://www.medrxiv.org/content/early/2024/09/26/2024.09.25.24314215}, <br>
	eprint = {https://www.medrxiv.org/content/early/2024/09/26/2024.09.25.24314215.full.pdf}, <br>
	journal = {medRxiv}
}
