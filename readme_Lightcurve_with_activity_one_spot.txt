### Project: Lightcurve_with_activity_one_spot.py

I completed this project during my postdoc in Göttingen, Germany (2021 - 2024).


### Project overview

This project aims at simulating synthetic light curves, i.e. flux time-series, where the flux comes from stars. The impact of internal magnetic fields on the surface of stars are included. The emergence of magnetic field lines at the stellar surface lead to the formation of active regions either darker (spots) or brighter (faculae) than the surrounding surface; those active regions are co-rotating with the surface of stars and their transit in front of the visible stellar disk results in a periodic variation of the flux, which can then be detected through a Fourier transform (done by the program Lomb_Scargle_periodogram.py).


### Methodology

The synthetic light curves are built from input physical parameters using physical equations and scaling relations, over a time span of 2 years that is close to the operation time of the PLATO space mission. In this approach, the active regions (dark spots and bright faculae) are circular with sizes much smaller than the radius of the star, appear instantaneously at 12 days at random longitudes, and their size decays linearly with time so that the active regions exist only for a given lifetime. The program uses as an input the file Kepler_bandpass_intensities.sav to take into account the fact that the contrast of an active region relative to the surrounding stellar surface depends on the wavelength and the position of the spot on the stellar disk; this file uses the spectral bandpass of the Kepler space mission, which is very close from the one of the PLATO space mission. The star is simulated either as differentially-rotating in latitude, i.e. the equator and the poles do not rotate on themselves at the same period, or rotating as a solid body, i.e. all latitudes rotate on themselves at the same period. The inclination of the rotation axis of the star with respect to the line-of-sight, the rotation period of the star, and the latitude of the active regions are additional input parameters that impact the resulting light curve.


### Results

The results are saved in ./Lightcurves_Aspot_15_MSH/* as .txt files; the files LC_fac_*.txt include the contribution to the flux of regions brighter than the surrounding stellar surface (i.e. faculae), the files LC_spot_*.txt include the contribution to the flux of regions darker than the surrounding stellar surface (i.e. spots), and the files LC_*.txt include the final light curves (i.e. the contributions to the flux of both faculae and spots). The files Parameters_*.txt contain physical parameters used to generate the synthetic light curves: if differential rotation between the equator and the poles of the star is implemented or not, the value of the period at which the star rotates on itself, a parameter scaling the level of magnetic activity caused by internal magnetic fields to use, an indicator of the level of magnetic activity, a parameter quantifying whether active regions appearing successively are nested or not, and the number of the realisation used to generate the ight curve (the longitude and time at which the active regions successively appear are random). The examples presented here include a total of 180 light curves that include only one dark spot located at the equator (latitude of 0 degrees), computed with the same rotation period of the star and with differential rotation in latitude; the light curves are computed for 2 different lifetimes for the spot (3 and 6 rotation periods of the star), and for 90 different inclination values for the rotation axis (from 1 degree to 90 degrees with a 1 degree step) for each given spot lifetime.


### Installation: with anaconda

git clone https://github.com/cgehan-astro/Postdoc_Germany_light_curves.git
cd Postdoc_Germany_light_curves
conda env create -f environment.yml
