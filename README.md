This repository contains the flow data and scripts used to generate Fig. 1 and Supplementary Fig. S1 and S2 in 'Promoter selection reduces phenotypic heterogeneity and improves bioproduction' (Patel et al.)

- Each folder contains the .csv files generated after data cleanup in FlowJo - the analysis of which is below.
- There are 3 biological replicates named either: 311020.../091120.../161220
- Use each folder with the script containing the same replicate name e.g. 311020 folders for use with '311020_run2_backup.R'
- The media condition is also in each folder name: 

ypd_exp = YPD exponential phase
ypd_sta = YPD stationary phase
ypd10_exp = YPD10 exponential phase
ypd10_sta = YPD10 stationary phase
mm_exp = YNB exponential phase
mm_sta = YNB stationary phase 
yepg_exp = YEPG exponential phase
yepg_sta = YEPG stationary phase

--------------------------------------------------------------------------------------------------------------
The R scripts:
The '...run2' scripts contain the diptest, mixed modelling analyses (for subpopulation identification) and plots generated following flow cytometry of the pYTK-sfGFP strains. Run the functions and then start from the 'mixedsort' function under each subsection to generate the analyses and plots from the paper.

Plate layouts and .fcs files can be made available upon request

--------------------------------------------------------------------------------------------------------------
Analysis in Flowjo used to generate the .csv files in each folder:

Controls:
GFP-/RFP+ = BP-HK = B9
GFP-/RFP- = BP- = B10
+GFP/RFP- = 897- = B11

The letter identifier of each control will change depending on the sample group. This is indicated within the '...run2' scripts

Flowjo analysis workflow:

1) singlets from phlum no pi (B10)
 - change axes to logical
 - apply to all in group

2) comp from B9-B11 
 - apply to all in group

3) Live/dead gating from BP-HK (B9) by comparing to BP (B8)
 - Live gate made as an offshoot of the singlets gate so 
   it is indented underneath it

4) Drag live gate of sample A1 and sample B8 (-ve control) into the layout
	and select comp bl1-h for the x-axis and histogram for y-axis

5) Set fonts of bl1h plot:
	Axis labels = 18
	Axis no. = 12
	Layout gates = 11
	Legend = 18

6) BL1-H values were exported as .csv files from the live population for further analysis in the '...run2' scripts. 

