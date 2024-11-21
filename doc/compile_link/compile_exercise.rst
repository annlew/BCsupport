.. _compile:

Compile and link exercise 
=====================

A basic Fortran compile and link excercise on Tetralith
+++++++++++++++++++++++++++

Download code from Github
-------------------------

Download the code and clear your environment

.. code-block:: text

   git clone https://github.com/annlew/compile_exercise.git 
   
   cd compile_exercise/compile

   module purge

In this folder you will find a basic **hello_world.f90** file and some Makefiles


Basic Makefile usage
-----------------------------------

Open the file **Makefile** and check what's inside.

Try to compile:

.. code-block:: text

   make

What happened?

Now, load a build environment and run make again, e.g.:

.. code-block:: text

   module load buildenv-intel/2023a-eb
   make

What is the difference? You might want to check the module investigation exercise :ref:`here <modules>`.
You should now have a working executable. Try to run:

.. code-block:: text

   ./hello_world.x

Type make again. What happens now?

Open **Makefile_2** and have a look. What is different compared to **Makefile**?

Do a clean up of the build directory:

.. code-block:: text

   rm hello_world.x
   rm hello_world.o

Build the executable using **Makefile_2**

.. code-block:: text

   make -f Makefile_2

And use **Makefile_2** to clean the build directory

.. code-block:: text

   make -f Makefile_2 clean
 
Open **Makefile_3** and have a look. What is different this time? Compile **hello_world** using **Makefile_3**.



Linking exercise
----------------------------------

In the folder compile you will also find **hello_nc_world.f90**. What is the difference between **hello_world.f90** and **hello_nc_world.f90**?
 
Rewrite the instruction in **Makfile_3** so that it compiles **hello_nc_world** instead of **hello_world** and compile. What happens?

We need a netCDF library. Check if that is available:

.. code-block:: text

   module avail netcdf

Load a netCDF module that is compatible with the compiler that you have chosen. Revise the module :ref: `exercise <modules>` again.

Open **Makefile_nc** and compare to **Makefile_3**. What is different?

Compile **hello_nc_world** using **Makefile_nc**:

.. code-block:: text

   make -f Makefile_nc

Run the executable. What was the result?







