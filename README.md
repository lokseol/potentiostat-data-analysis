# CV, GCD and EIS Data Analysis
This code is designed to analyze the data measured by a potentiostat: 
cyclic voltammetry (CV), galvanostatic charge and discharge (GCD), and electrochemical impedance spectroscopy (EIS). 
It reads primary data from the raw files, extracts the primary parameters, and then calculates the performance parameters such as capacitance, energy, and power. 
This code is optimized for Biologic potentiostat such as SP-150, but can be applied to other files with some modifications (i.e. headerline number and column name).

## How to use
Install pandas and matplotlib libraries.
Change the AL_mass and Area_two_elec according to the measured value.
Place CV, GCD, and EIS data files in the "Input_data" folder.
Run the script to generate the plots and summarizing table.

## Functions
The code provides the following functions:

read_file_CV(filename, headerline): imports CV data file, cleans it, and extracts primary parameters.\
calculate_sec_param_CV(data, scan_rate, Vmax, AL_mass, Area_two_elec): calculates performance parameters from a CV curve.\
read_file_GCD(filename, headerline): imports GCD data file, cleans it, and extracts primary parameters.\
calculate_sec_param_GCD(data, I_gcd, Q_disc, Vmax, AL_mass, Area_two_elec): calculates performance parameters from a GCD curve.\

## Note
The headerline argument of the read_file_CV, read_file_GCD, and filtering_EIS functions may need to be changed depending on the file condition.
Their default values are 52, 48, 58, respectively.
If an error still occurs, also change the numbers of # at the headerline-# parts.

Example results are shown in the CV-GCD-EIS combined.ipynb
