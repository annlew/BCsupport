# Modules on Tetralith

## What is a module and what does it do?

Useful module commands:

    module avail
    module load
    module list
    module show
    module purge


Module investigation exercise:


    module avail
    module avail netcdf
    module list
    module load buildenv-intel/2018b-eb
    module avail netcdf
    module list
    module load netCDF/4.3.2-HDF5-1.8.12-nsc1-intel-2018.u1-bare
    module show netCDF/4.3.2-HDF5-1.8.12-nsc1-intel-2018.u1-bare
    echo $NETCDF_DIR
    echo $PATH
    echo $PATH | grep netcdf
    module show buildenv-intel/2018b-eb

What is netCDF/4.3.2-HDF5-1.8.12-nsc1-intel-2018.u1-bare?

    module show netCDF/4.3.2-HDF5-1.8.12-nsc1-intel-2018.u1-bare 
    vi /software/sse/modules/netCDF/4.3.2-HDF5-1.8.12-nsc1-intel-2018.u1-bare.lua
    ls $NETCDF_DIR

    v /software/sse/manual/netcdf/4.7.4/HDF5-1.10.8-nsc1-gcc-7.3.0-bare/build.txt

    ls /proj/bolinc/shared/software/apps/

Check your environment

    printenv
    printenv | grep netcdf
    module purge
    printenv
    printenv | grep netcdf
   

