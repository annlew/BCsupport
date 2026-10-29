. _OIFS:

Compiling OIFS on Arrhenius
===============================

Preparations
++++++++++++

The installation has been tested with the following modules::

    module load buildenv-intel/2025b-eb netCDF/4.9.3 netCDF-C++4/4.3.1 netCDF-Fortran/4.6.2

The intel compiler variables need to be exported::

    export FC=mpiifort
    export CC=mpiicc
    export CXX=mpiicpc

These settings are included in the Arrhenius configuration file.

/nobackup/proj/disk/bolinc/personal/annlew/OIFS/openifs-expt/ab7z/2016092500/run-oifs.arrhenius.job

Download code (cf. https://github.com/ecmwf-ifs/openifs)::

    git clone --depth 1 --branch openifs-48r1.1.0 --single-branch https://github.com/ecmwf-ifs/openifs.git openifs-48r1.1.0


A configuration file that can be used for compiling and running installation tests can be found here::

    /nobackup/proj/disk/ecearth3_input-data/shared/OpenIFS/oifs-config.arrhenius.sh

Copy to your installation directory and source::
 
    source oifs-config.arrhenius.sh


Not that you might have to set the explicit path to your installation directory when you start production runs.

Configure and download bundle::

    $OIFS_TEST/openifs-test.sh -c

Before building, in the following file (for atlas v0.34.0, which is default bundle setting for c48r.1.1.0)::

    source/atlas/src/atlas/field/detail/FieldImpl.h

add the following line::
     
    #include <algorithm>

Build using the debug option::

    $OIFS_TEST/openifs-test.sh -b --build-type=DEBUG

The code will be compiled with -g -O0 instead of -g -O2 -march=core-avx2 -no-fma

The tests need to be run on a compute node since the log in node does not allow the amount of memory needed for runnign the tests::

    interactive -A project -n 1 -t 00:30:00
    $OIFS_TEST/openifs-test.sh -t




