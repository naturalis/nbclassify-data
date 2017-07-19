This folder contains tabular data that resulted from either manual or automated counts. The following files 
were produced by automated counting:
- foto_data.tsv - photos submitted by volunteers
- foto_data_professioneel.tsv - photos taken with professional camera
- foto_data_wileyfox.tsv - photos taken with WileyFox camphone
These tables were produced by the following workflow:
1. the analysis script https://github.com/naturalis/nbclassify/blob/sticky-traps/html/sticky_traps/analyze.py operates on the 
   specified folder or file, and emits tab separated data
2. to these tables were manually added the columns with capital labels, which would normally be added by the web application

In addition, there is a file of manually counted traps (getelde_insecten_per_val.tsv) with the same columns. The data in this
table are reference data against which the image processing is validated. The different tables can be joined on the combination
of `Bedrijf` + `Beheertype` + `Valnummer` + `Datum`, as was done in the *.Rmd file.


./Photos contains the images used in the analyis. These photos have been sorted by camera used.