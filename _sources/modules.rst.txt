.. _modules:

Modules on Tetralith
======================

What is a module and what does it do?
++++++++++++++++++++++++++++++++++++++++

Useful module commands:

.. code-block:: text

    module avail
    module load
    module list
    module show
    module purge


Module investigation exercise:

.. code-block:: text

    module avail
    module avail netcdf
    module list
    module load buildenv-intel/2023a-eb
    module avail netcdf
    module list
    module load netCDF-HDF5/4.9.2-1.12.2-hpc1
    module show netCDF-HDF5/4.9.2-1.12.2-hpc1
    echo $NETCDF_DIR
    echo $PATH
    echo $PATH | grep netcdf
    module show buildenv-intel/2023a-eb

What is netCDF-HDF5/4.9.2-1.12.2-hpc1 

.. code-block:: text

    module show netCDF-HDF5/4.9.2-1.12.2-hpc1
    vi /software/sse2/tetralith_el9/supplemental-modules/buildenv-intel/2023a-eb/netCDF-HDF5/4.9.2-1.12.2-hpc1.lua
    ls $NETCDF_DIR

    v /software/sse2/tetralith_el9/manual/hdf5_netcdf-c-fortran/hdf5-1.12.2_netcdf-4.9.2/nsc1-intel-2023a-eb/build.txt


Check your environment

.. code-block:: text

    printenv
    printenv | grep netcdf
    module purge
    printenv
    printenv | grep netcdf
   

