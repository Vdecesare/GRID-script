# GRID-script
Script to select Ubiquitin and 15N Ubiquitin m/z and report them in the same position as spotted on a 1536 MALDI plate
READ ME

1. System requirements: the script relies on a Windows Batch File (.bat) and an Executable Jar File (.jar). It therefore requires a windows system and Java to be installed. Version of windows tested: windows XP and windows 7. 

Java version tested: Version 8 Update 131 (build 1.8.0_131-b11)

2. Installation guide: Install Java software (Version 8 Update 131 (build 1.8.0_131-b11)) and Java (TM) Platform SE Binary. 
Copy the Misc folder (containing the GRID file) on your root (C:) local drive (no installation required). 

Save your FlexAnalysis peak picking output as .txt file (a Test.txt file is available as demo in the GRID folder). This file will contain area intensity of both ubiquitin signal (8565.76 m/z) and 15N ubiquitin (8669.47 m/z). 

The script expects a parameter file called maldiGridOmaticParams_*.txt (in the same directory as the input file) containing min/max range for both Light and 15N ubiquitin m/z values. 


3. Instructions to run on data
Drag and drop Test.txt file (or your result file) on "runMaldiGridOmaticatic". 

Data output will be created in the same directory and will be called Test_GRID.txt (assuming your input file was Test.txt). 

If the output file already exists, then a datestamp will be added to the file output. 

The output GRID file will have a 1536 well grid of masses and intensities repeated for each parameter as for maldiGridOmaticParams. 


Notes/assumptions:

there can be multiple entires per spot (as you would expect form peak picking), only those masses matching the parameter min-max values will be used.

There should be only one entry per spot that matches the parameters.  If there are multiple entries for the same spot within the min-max value pairs, then a CAUTION note will be output to the terminal/cmd window. 

Parameters ranges should not overlap, otherwise the data analysis will be uninformative.
