In our tutorial, we will perform some quantitative phase analysis of powder X-ray diffraction.  

We will start with "looking under the hood" with the Rietveld method by inspecting an excel spreadsheet set up to analyze data for TiO<sub>2</sub> by Professor John Evans (University of Durham); more information found here: https://johnevans.webspace.durham.ac.uk/tutorial_riet_excel/. 

We will use `excel_rietveld_01.xlsx` for this exercise.  

For a more practical tutorial for your own research activities, we'll be using the open-source software package, GSAS-II:

https://advancedphotonsource.github.io/GSAS-II-tutorials/

You can install the software on windows, mac, or linux: https://advancedphotonsource.github.io/GSAS-II-tutorials/install.html

It would be helpful to install this prior to class.  

We will do some analysis on different data sets collected on the Bruker D8 DaVinci powder X-ray diffractometer located in the Analytical Resources Core at Colorado State University. The data are saved in the proprietary Bruker `brml` format.  If you need to convert formats, you can use a conversion tool that I have written: https://github.com/jrneilson/xrdconversion.  

Here are the samples:

* LaB<sub>6</sub> diffraction standard.  `LaB6_10-130_100min_NiFilt_spin_antiscat_070925.brml`

* Al<sub>2</sub>O<sub>3</sub>, chemical grade.  `Al2O3_std_10-130_100min_NiFilt_spin_antiscat_070125.brml`

* ZnO, chemical grade, annealed at 700 °C for 2 hours: `ZnO_700c_2hrs15minHeat_45minScan_0.0357stepsize_0.77steptime.brml`

A "Mason Stain" powder used for glazing ceramics (6006 Deep Crimson; aka Chrome Tin Pink Sphene).  `Mason_Stain_6006_10-120_1secperstep_spin_antiscat_NiFilt_070725.brml` 

Data were collected in Bragg-Brentano geometry.  In instrument parameters are defined within `D8DaVinci_20261020.instprm` for setting up the quantitative analyses in gsas-II.  The Mason Stain, LaB<sub>6</sub>, and Al<sub>2</sub>O<sub>3</sub> data were collected with a Ni filter in front to the detector to block a contaminating X-ray wavelength from tungsten.  

We will use the various `cif` files as structural models for our analysis.  

