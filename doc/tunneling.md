# Tunneling on Tetralith

## Notebook on compute node

Start an interactive jobLoad a Python module e.g.:

    module load Python/3.8.3-anaconda-2020.07-extras-nsc1

Start a jupyter notebook and specify the node you are working on:

    jupyter-notebook --no-browser --ip=nXX

example:

    [x_alewi@n19 ~]$ jupyter-notebook --no-browser --ip=n19

You will get something like:

    [I 11:13:55.182 NotebookApp] The Jupyter Notebook is running at:
    [I 11:13:55.182 NotebookApp] http://n19:8888/?token=58a74ec25157356a51e655bca3c47069396d211ebbe2d9e3

    To access the notebook, open this file in a browser:

    file:///home/x_alewi/.local/share/jupyter/runtime/nbserver-243891-open.html
    
    Or copy and paste one of these URLs:

        http://n19:8888/?token=58a74ec25157356a51e655bca3c47069396d211ebbe2d9e3
     or http://127.0.0.1:8888/?token=58a74ec25157356a51e655bca3c47069396d211ebbe2d9e3

Note the node name (n19) and the port, in this example: 8888

In another terminal, make an ssh tunnel log in, note the node name and port:

    ssh -N -L localhost:8888:n19:8888 x_user@tetralith.nsc.liu.se

Then, in a browser, copy paste the equivalent link:

    http://127.0.0.1:8888/?token=58a74ec25157356a51e655bca3c47069396d211ebbe2d9e3

If you only get a link with node name which the browser fails to connect to, try another Python module


