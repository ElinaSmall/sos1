# sos1

Pipline:

01. Chembl v.36 compounds ~5k  related to SOS1 target protein + all known patented compounds from Bind PDB ~7k were collected, cleaned, united (Train set)

02. For fast pre-screening of 1.6M compounds from ChemDiv database ML models XGBoost and Random Forest were employed (collected ~50 compounds). 
Decoys were selected as random ceneter clusters from the whole chembldb after splitting by Bemis-Murco scaffolding. 

03. Ultra-fast Tanimoto similarity search was presented based on all known chembl and patented compound vs 1.6M compounds from ChemDiv.
Intermediate datasets include ~30-115k compounds for virtual screening (depending on threshold variable).

04. Pre-docking preparation. Download, alignment of all proteins. detection of 2 main binding sites. Redocking of known ligands. Validation of docking. 

05. Smina physic-based virtual pre-screening (as fast cpu-based).
 
> Next steps:

- Detect docking energy cutoff (minimizedAffinity)
- Ensemble docking for binding site 1 and bindig site2, rmsd mcss plots.
- Selecting of 1-10 ligands for visual review based on critical bondings (prolif) and validate with Induced Fit Docking (Scroedinger protocol)/ Molecular Dynamics 


