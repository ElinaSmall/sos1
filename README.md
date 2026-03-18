# sos1

Pipline:

01. Chembl v.36 compounds ~5k  related to SOS1 target protein + all known patented compounds from Bind PDB ~7k were collected, cleaned, united (Train set)

02. For fast pre-screening of 1.6M compounds from ChemDiv database ML models XGBoost and Random Forest were employed (collected ~50 compounds). 
Decoys were selected as random ceneter clusters from the whole chembldb after splitting by Bemis-Murco scaffolding. 

03. Tanimoto similarity search was presented with minimal possible threshold (0.45) based on all known chembl and patented compound vs 1.6M compounds from ChemDiv.
Intermediate dataset include 115k compounds for virtual screening.

04. Pre-docking preparation. Download, alignment of all proteins. detection of 2 main binding sites. Redocking of known ligands. Validation of docking. 

05. Smina physic-based virtual pre-screening. 
