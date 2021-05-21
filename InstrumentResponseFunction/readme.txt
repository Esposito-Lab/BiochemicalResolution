These scripts use Fisher information and Monte Carlo simulations to evaluate how the instrument response function causes loss in information and how these losses propagate to deteriorate the resolution of FLIM systems applied to biochemical imaging. 
Developed for the research article: 
A. L. Trinh, A. Esposito, "The biochemical resolving power of fluorescence lifetime imaging: untangling the roles of the instrument response function and photon-statistics"

There are 4 scripts:
'DiracIRF_FisherInformation_V1.nb'
-Validates our Fisher information approach by reproducing Fig. 1 in Kollner and Wolfrum. 
-After validating, we will then use the same approach to include a Gaussian IRF in the next script to understand its role in measurement precision.

'GaussianIRF_FisherInformation_V1.nb'
-Using Fisher information, it evaluates the role of a Gaussian IRF on measurement precision.
-Generates the file 'GaussianForMatlab.mat'. This file contains the F-values for various IRF Gaussian widths.

'IRF_MCSimulations.ipynb'
-Using Monte Carlo simulations, it evaluates the role of IRFs on measurement precision.
-Validates by reproducing Fig. 1 in Kollner and Wolfrum and also Gaussian results from our Fisher information analysis.
-In addition, it evaluates aspects that are more challenging to perform using Fisher information, including evaluating different IRF shapes and fitting.
-Generates the files: 'F_dirac.npy', 'F_known.npy', 'F_unknown.npy', 'F_knownsq.npy'. These are files containing F-values for dirac IRF, Gaussian IRFs, Gaussian IRFs where the IRF is fitted, and Rectangular IRFs, respectively.

'IRF_Plots.ipynb'
-Loads in previously generated F-values and generates plots.
-Loads the files: 'GaussianForMatlab.mat', 'F_dirac.npy', 'F_known.npy', 'F_unknown.npy', and 'F_knownsq.npy'

Example generated data is included as:
'GaussianForMatlab.mat'
'F_dirac.npy'
'F_known.npy'
'F_unknown.npy'
'F_knownsq.npy'