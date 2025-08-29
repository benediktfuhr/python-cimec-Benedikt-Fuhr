# python-cimec-Benedikt-Fuhr
Final Project of the Cimec-Python course 2025 by Luigi Petrucco

Turbulence project 

In this project, the Turbulence dynamics framework is applied on resting-state MRI data of autistic individuals. It uses part of the open-source dataset ABIDE (ABIDE I and II, Di Martino et al. 2014, 2017). This dataset consists of resting-state MRI scans of both, autistic as well as typically developed individuals. Additionally, it provides phenotypical data of the subjects (such as age, sex, handedness, IQ-scores, etc.), as well as scanner specifics. 

We want to investigate the hypothesis that autistic individuals show altered turbulent markers in the brain compared to TD individuals. To operationalize this, we use the turbulent-dynamics framework from Deco and Kringelbach, 2020. In short, the turbulent dyncamics framework uses formalizations from fluid-dynamics theory from physics to apply on the human brain. In their seminal paper, Deco and Kringelbach found such turbulent markers in the human brain. To simplify things in this project, we only compute two metrices: Metastability and Global Synchronization. These two metrices are measures of how variable (Metastability) and how strong in magnitude (Global Synchronization) synchronization is in the whole-brain. This is done by using Hilbert-transformed Phase data from the ABIDE dataset. This transformation was done already in a previous analysis - here we only use the Phase- and Phenotypical data from the ABIDE dataset. 

The project has this outline: 
    1) Loading in the phase and phenotypical data for one subject 
    2) Creating a meaningful data-format for this subject for further analysis
    3) Computing the Metastability and Global Synchronization value for this subject
    4) Visualizing what these metrices mean and how they are computed 
    5) Repeating steps 1-3 for all subjects
    6) Visualizing group-level statistics for Metastability and Global Synchronization 

What is needed to run the code? 

    -   On your local machine, in a location of your choice, create a folder called "data".
    -   Inside the "data"-folder create a subfolder called "mri". Download the .mat files from GitHub and store the downloaded files inside the "mri"-folder
    -   Inside the "data"-folder create another subfolder called "pheno". Download the phenotypical data (pheno.csv) and the motion related data (motion.csv) from GitHub and store them inside the "pheno" folder
    -   Change the "root" variable in the Python script to the folder where the "data"-folder is stored 

