# AI_and_Drug_Discovery_Course_2026
## Assignment 2: QSAR Data Curation from ChEMBL

### Selected Target
Target Name: Epidermal Growth Factor Receptor (EGFR)
ChEMBL ID: CHEMBL3608
EGFR is a clinically important receptor tyrosine kinase involved in cancer development and progression.

### Bioactivity Data
Bioactivity Type: IC50
Unit: Nanomolar (nM)
Number of Bioactivity Records: 160 total and 94 (Obtained after filtering valid IC50 values and SMILES entries)

### Data Curation Workflow
The workflow includes target identification, retrieval of IC50 bioactivity data from ChEMBL, filtering of missing or invalid records, preprocessing of molecular data and saving the curated dataset in CSV format for QSAR modeling.


## Assignment 3: Exploratory Data Analysis & Descriptor/Fingerprint Calculation

### Dataset Summary
Number of molecules: 76 curated molecules
Columns: SMILES, ChEMBL IDs, pIC50, bioactivity class, Lipinski descriptors, PaDEL 2D descriptors and fingerprints

### Exploratory Data Analysis (EDA)
#### pIC50 values: 
ranged from 3.0 to 11.36, with an average of 5.70 and a standard deviation of 2.08, showing diverse compound potency
#### Visualizations:
Histogram of pIC50 distribution
Bar plot showing counts of active vs inactive compounds
#### Statistical Analysis: Mann–Whitney U test indicated:
Number of Hydrogen Bond Acceptors (NumHAcceptors) is significantly different between active and inactive compounds
Molecular Weight, LogP, and Number of Hydrogen Bond Donors were not statistically significant

### Descriptors and Fingerprints
#### Lipinski Descriptors (calculated using RDKit):
Molecular Weight (MW)
LogP
Number of Hydrogen Bond Donors
Number of Hydrogen Bond Acceptors
#### PaDEL 2D Descriptors (calculated using PaDELpy): 
1444 descriptors providing detailed molecular features relevant to EGFR activity
#### Fingerprints (calculated using PaDELpy):
PubChem fingerprints: 881 bits
Substructure fingerprints: 307 bits

### Why PaDELpy was chosen
Widely used and reliable for QSAR studies
Allows calculation of standardized descriptors and fingerprints
PubChem fingerprints are fixed-length and suitable for machine learning
Substructure fingerprints capture detailed chemical patterns relevant to EGFR bioactivity
