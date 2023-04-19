
SFG microscopy data were processed using WOLFRAM MATHEMATICA (ver. 12.3.0) to produce SFG mapping images and locally averaged SFG spectra. The attached code was tested with version 12.3.0 and worked well on both Windows and macOS. You can download and install WOLFRAM MATHEMATICA here: www.wolfram.com/mathematica. It does not require any non-standard hardware. However, it may need decent PC performance to use. Since Mathematica is commercial software, the details of installation instructions and PC specifications are not described here but are available on the website. The installation should be finished within 1-20 minutes. The time may vary depending on the version and your PC performance.

* Instructions to use *

In the folder, there are four files:
1. Readme.txt
2. Onion epidermis Horizontal.nb
3. Two raw data in .asc extension for demo

'Onion epidermis Horizontal.nb' is the custom Mathematica codes to produce SFG maps, and the two .asc files are the raw data from the experiments.

Onion epidermis Horizontal data process:
Before running the code, make sure the two .asc files are in the same folder where .nb file is located. The file path was already properly inserted. Otherwise, you need to insert the file path of the .asc files to the "Import[]" in section A-2 correctly. 

How to run the code:
1. Open "Onion epidermis Horizontal.nb" file
2. On the top menu bar, click "Evaluate" - "Evaluate Notebook".
3. It takes a few minutes to complete, and the results are saved as .csv file in the same folder where the .nb file is located. SFG maps are produced in the Mathematica code files. The error messages starting with "Part:" and "General:" in the Data exportation section can be ignored.

The explanation for the result files:
1. SFG mapping images can be directly copied in the .nb files and pasted to the Powerpoint or Word.
2. Three excel files are saved: "Onion epidermis Horizontal_avgall", "Onion epidermis Horizontal_avgHVF", and "Onion epidermis Horizontal_regions 1-n".
3. The first one ("..._avgall") is the averaged SFG spectrum over the whole scanned area, the second ("..._avgHVF") has the averaged SFG spectra of the horizontal edges (longitudinal edges), the vertical edges (transverse edges), and the face region separately. The last one ("..._regions 1-n") has the individual SFG spectra of the regions; the region 1-20 are the longitudinal edge regions, the region 21-40 are the transverse edge regions, and the region 41-60 are the face regions.
4. In the last "..._regions 1-n" excel file, some columns have the text starting with "Mar" instead of numbers. This is because the regions were not assigned, and can be ignored. 

--- end ---

--- additional notes ---
* SFG microscopy data processing requires manual region assignments by typing coordinates in Section C-2, which vary depending on the datasets. Thus, the regional SFG spectra averaging (Section C-2) in the two .nb files only work with the two .asc datasets in the folder. However, the SFG mapping section works for other .asc datasets with the correct scan size and step distance.

* In the code, the parts that produce the main text figure (Figure 1) are highlighted in yellow. 

* Please note that the code may not work when the file is located where the file path name is too long or when the file name includes special characters.

* More about the raw data: each pixel has 1024 x 2 data points (one spectrum), and the four .asc files have total 900 scanned pixels (30 x 30). All 900 data are saved in two-column data in (900*1024, 2). Using the broadband SFG system, two SFG spectra are collected per sample and combined in the code; one covers the CH region (2750-3050 cm^-1), and the other covers the OH region (3200-3500 cm^-1).   

* More about the raw data import: in section A-2, there are two "Import[]" syntaxes. "data1=Import[]" is to import CH region spectra, and "data2=Import[]" is to import OH region spectra. The current file path was highlighted in light gray. For the "Onion epidermis Vertical.nb" file, "15mst pps O5 H 30x30(10)_ch_833.asc" and "15mst pps O5 H 30x30(10)_oh_832.asc" are for CH and OH spectra, respectively.)

