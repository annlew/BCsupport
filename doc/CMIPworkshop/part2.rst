.. _part2:

CMIP workshop part 2
===============================
here is a pdf file :download:`pdf <images/klaus.pdf>`

   .. image:: images/klaus.pdf
     :width: 600
     :alt: Missing image file


Practical part
++++++++++++

Outline

* Recap of part 1
* Which type of data access makes sense for your data processing?
* CMOR post-processing and QA

Working with CMIP data - other ways of access than ESGF web portal
----------------

**Server-side data storage**

| IS-ENES (ended in 2023 but great portal)
| https://is.enes.org/

| SMHI (Bolin Centre) data library
| Available on Tetralith but requires permission

**Large scale data download and synchronisation with ESGF**

| ESGpull
| https://esgf.github.io/esgf-download/

Data format - CMOR and CMORisation
----------------

| CMOR - Climate Model Output Rewriter
| https://cmor.llnl.gov/

| CMOR tables
| https://github.com/PCMDI/cmip6-cmor-tables/tree/main

| Conversion table from native model variable to CMOR format - NorESM example
| https://github.com/NorESMhub/noresm2cmor/blob/master/namelists/CMIP6_NorESM2-LM/historical/template/var.nml


Exploring CMIP data
------------------------

**Your task**

* Find monthly mean precipitation flux for SSP2-4.5 from NorESM2-LM
* How many members are there?
* What is the model resolution of the atmosphere component?
* Available variants?
* Available dataset version(s) for say r1i1p1f1?
* On which server are the data located? Are there any replicas anywhere?
* How many files are in r1i1p1f1?
* Download the r1i1p1f1 dataset
* Inspect metadata in one of the netCDF files with ncdump
* Look at the data with ncview
* Load data in jupyter notebook/python/other plotting tool and make plots (maps and timeseries)


**Questions**
