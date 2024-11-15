.. _conda:

Conda on Tetralith
====================

Create an environment:

.. code-block:: text

    module load Anaconda/2023.09-0-hpc1
    conda create -n fredagsmys
    conda activate fredagsmys
    python --version
    which python

    conda install python=3.8
    python --version
    which python

    conda list (-n fredagsmys)  

    conda deactivate

Where are your environments?
 
.. code-block:: text

    cd
    ls -a
    ls -lrt .conda
    du -hd 1 ./

    conda clean --all  


Store away your environments

.. code-block:: text

    conda env export --name fredagsmys > fredagsmys.yml
    conda env export --from-history --name fredagsmys > small_fredagsmys.yml
    conda env list

    conda env remove -n fredagsmys
    conda env list

    conda env create -n fredagsmys -f fredagsmys.yml
    conda env list

   

