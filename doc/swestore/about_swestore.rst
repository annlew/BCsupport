.. _about_swestore:

About Swestore
====================

Documentaion
++++++++++++++++++++

Swestore documentation can be found on this web page `<https://docs.swestore.se/>`_


Access
+++++++++++++++++++

All members of the Bolin Centre storage project also have access to the Bolin Centre's Swestore storage. You can find your Swestore username in the `SUPR <https://supr.naiss.account/>`_ portal under "Accounts" in the menu to the left. Here you can also set your Swestore password.

Quota
+++++++++++++++++++

Our current quota and usage can be found on the SUPR project page for the active storage project.


What can you store on Swestore?
+++++++++++++++++++++++++++++++

The Bolin Centre Swestore storage is intended for large coherent datasets that, e.g. raw data from climate model simulatios, that needs to be kept, but is not being heavily processed. The data needs to be documented and have an exipry date. Swestore is not a back up service.

Storage policy
+++++++++++++++++++

Only large coherent data sets that need to be stored for a long time and reused should be stored on Swestore. The data should be stored based on model/production method, responsible PI, producer and data set, e.g.:

.. code-block:: text
    swestore:/snic/bolinc/MODEL/PI/PRODUCER/DATASET

    swestore:/snic/bolinc/NorESM1/AnnicaEkman/x_alewi/7xEU_OC

A data description README file has to be uploaded which describes the data, along with configuration scripts and namelists.

Example
.. code-block:: text
   Template for mandatory information for data upload on Swestore
   
   Generation method, e.g. Model+version
   
   Owner/producer including affiliation
   
   Project/PI/Secondary owner
   
   Expected lifetime, expiry date (latest end of contract)
   Short description of data
   
   Data format, e.g. netCDF, grib
   
   Time coverage
   
   Time step
   
   Plus configuration scripts and namelists with info about input data (BC and IC)





    An expiry date for the data set has to be provided, indicating when the data will be deleted or further storage reviewed.

   

