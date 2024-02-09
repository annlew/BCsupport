.. _vscode:

VSCode on Tetralith
=====================

Notebook through VSCode
+++++++++++++++++++++++

1. Start VSCode on your local machine. You will need the following extensions:

* Jupyter
* Remote - SSH
* Remote Explorer
* Python

2. Connect to Tetralith by clicking the button in the lower left corner "Open a Remote Window".

   .. image:: /images/remote.png
     :width: 600
     :alt: Missing image file

3. In the prompt that will appear at the top of the window, click on "Connect to Host". If this is the first time you connect to Tetralith through VSCode, choose "+ Add New SSH Host" 

   .. image:: /images/remote_ssh.png
     :width: 600
     :alt: Missing image file

   Enter ssh x_username(at)tetralith.nsc.liu.se. You will be prompted to updade your SSH configuration file.
 

4. Go back to step 2 and select tetralith in the drop down menu. Enter your log in credentials.

5. You might need to reinstall/enable Jupyter for remote host. Check the extension manager. 

6. Open a terminal in VSCode (in the "Terminal menu"). Load an Anaconda module and activate an environment. Instructions for how to work with conda environments on Tetralith can be found :ref:`here <conda>`

7. Go to "File" and click "New file...". Select Jupyter Notebook from the drop down menu that appears.

8. Once the notebook is open, you can choose which environment you would like to use. Click on "Select kernel" in the upper right corner

   .. image:: /images/kernel.png
     :width: 600
     :alt: Missing image file

   Click on the environement you would like to use.

9. You will now be running your notebook on the Tetralith log in node.

