# SiCNMF
Computes phenotypes using SiCNMF algorithm described in 
***
Please cite above work if using this code.

#####
REQUIREMENTS:
python, 
python packages: numpy, scipy, sklearn

#####
HOW TO USE:
1. Fill in the input parameters in SiCNMF.config file (should be in the same directory as SiCNMF_start.py). Replace the sample inputs in the file.
2. Run the following command in a terminal:
python SiCNMF_start.py

#####
INPUTS: 
---model: CNMF for no sparsity inducing factors or SiCNMF 
---sources: Comma separated list of sources of patient data to be used in SiCNMF
---Xfiles: Comma separated list of flat file names containing EHR data. Each file should be an .npy file containing a sparse matrix of EHR data of patients x source data. Check: numpy.load(<.npy filename>).ravel()[0] should return a sparse matrix of size nPatients x nSourceItems.
---nFactors: Number of latent factors/phenotypes to return
---[optional]outdir: Relative path to the directory to save output files. Default='./'
---[optional]etaSweep: Comma separated list of paramter values of eta to evaluate SiCNMF on. Default=[1]

#####
OUTPUTS:
#####
