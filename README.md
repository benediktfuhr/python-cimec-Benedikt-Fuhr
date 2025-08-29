# Final Project for the Cimec-Python course 2025 by Luigi Petrucco

# Summary of the Turbulence Project 
In this project, the Turbulence dynamics framework (Deco and Kringelbach, 2020) is applied on resting-state MRI data of autistic individuals. It uses part of the open-source dataset ABIDE (ABIDE I and II, Di Martino et al. 2014, 2017). This dataset consists of resting-state MRI scans of both, autistic as well as typically developed individuals. Additionally, it provides phenotypical data of the subjects (such as age, sex, handedness, IQ-scores, etc.), as well as scanner specifics. 

# Project background and aims
This project investigates the hypothesis that autistic individuals show altered turbulent markers in the brain compared to TD individuals. To operationalize this, the turbulent-dynamics framework from Deco and Kringelbach, 2020 is applied. In short, the turbulent dyncamics framework uses formalizations from fluid-dynamics theory from physics and applies it on the human brain. In their seminal paper, Deco and Kringelbach found such turbulent markers in the human brain. Very simmplified, turbulenct markers are considered to facilitate information transfer and efficiency in any complex system. To simplify things in this project, we only compute two metrices that are linked to Turbulence: Metastability and Global Synchronization. These two metrices are measures of how variable (Metastability; see Hancock et al., 2025) and how strong in magnitude (Global Synchronization) synchronization is in the whole-brain. This is done by using Hilbert-transformed Phase data from the ABIDE dataset. This transformation was done already in a previous analysis - here we only use the Phase- and Phenotypical data from the ABIDE dataset. 

# Outline of the Project
    1) Loading in the phase and phenotypical data for one subject 
    2) Creating a meaningful data-format for this subject for further analysis
    3) Computing the Metastability and Global Synchronization value for this subject
    4) Visualizing what these metrices mean and how they are computed 
    5) Repeating steps 1-3 for all subjects
    6) Visualizing group-level statistics for Metastability and Global Synchronization 

# What is needed to run the code? 

    -   On your local machine, in a location of your choice, create a folder called "data".
    -   Inside the "data"-folder create a subfolder called "mri". Download the .mat files from the data/mri folder and store the downloaded files inside the "mri"-folder
    -   Inside the "data"-folder create another subfolder called "pheno". From the data/phenom, download the phenotypical data (pheno.csv) and the motion related data (motion.csv) and store them inside the "pheno" folder
    -   Change the "root" variable in the Python script to the folder where the "data"-folder is stored 

# Literature 

Deco, G., & Kringelbach, M. L. (2020). Turbulent-like Dynamics in the Human Brain. Cell Reports, 33(10), 108471. https://doi.org/10.1016/j.celrep.2020.108471

Di Martino, A., O’Connor, D., Chen, B., Alaerts, K., Anderson, J. S., Assaf, M., Balsters, J. H., Baxter, L., Beggiato, A., Bernaerts, S., Blanken, L. M. E., Bookheimer, S. Y., Braden, B. B., Byrge, L., Castellanos, F. X., Dapretto, M., Delorme, R., Fair, D. A., Fishman, I., … Milham, M. P. (2017). Enhancing studies of the connectome in autism using the autism brain imaging data exchange II. Scientific Data, 4, 170010. https://doi.org/10.1038/sdata.2017.10

Di Martino, A., Yan, C.-G., Li, Q., Denio, E., Castellanos, F. X., Alaerts, K., Anderson, J. S., Assaf, M., Bookheimer, S. Y., Dapretto, M., Deen, B., Delmonte, S., Dinstein, I., Ertl-Wagner, B., Fair, D. A., Gallagher, L., Kennedy, D. P., Keown, C. L., Keysers, C., … Milham, M. P. (2014). The autism brain imaging data exchange: Towards a large-scale evaluation of the intrinsic brain architecture in autism. Molecular Psychiatry, 19(6), 659–667. https://doi.org/10.1038/mp.2013.78

Hancock, F., Rosas, F. E., Luppi, A. I., Zhang, M., Mediano, P. A. M., Cabral, J., Deco, G., Kringelbach, M. L., Breakspear, M., Kelso, J. A. S., & Turkheimer, F. E. (2025). Metastability demystified—The foundational past, the pragmatic present and the promising future. Nature Reviews Neuroscience, 26(2), 82–100. https://doi.org/10.1038/s41583-024-00883-1

Power, J. D., Barnes, K. A., Snyder, A. Z., Schlaggar, B. L., & Petersen, S. E. (2012). Spurious but systematic correlations in functional connectivity MRI networks arise from subject motion. NeuroImage, 59(3), 2142–2154. https://doi.org/10.1016/j.neuroimage.2011.10.018

