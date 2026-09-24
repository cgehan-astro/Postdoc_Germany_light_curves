### Organisation of the repository

There are 2 programs in this repository.


### 1. Lightcurve_with_activity_one_spot.py: description in readme_Lightcurve_with_activity_one_spot.txt

This program takes as an input the file Kepler_bandpass_intensities.sav and produces as outputs the files *.txt contained in ./Lightcurves_Aspot_15_MSH/*.


### 2. Periodogram.py: description in readme_Periodogram.txt

This program takes as an input the files *.txt contained in ./Lightcurves_Aspot_15_MSH/*. as well as the file Example_PLATO_LC_PSLS_no_systematics_no_activity_no_granulation_P1_NSR_50_ppm.dat, and produces as outputs the plots Light_curve_1_spot_3_rotation_periods.pdf, Light_curve_1_spot_6_rotation_periods.pdf and Lomb_Scargle_periodogram.pdf.


### Installation: with anaconda

git clone https://github.com/cgehan-astro/Postdoc_Germany_light_curves.git
cd Postdoc_Germany_light_curves
conda env create -f environment.yml
