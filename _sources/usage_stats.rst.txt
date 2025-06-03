Check usage
===========

How to check usage statistics
----------------------------

Useful commands::

    storagequota
 
Shows how much space you use in each project and how many files you store ::

    projinfo 

Shows how much computing time that has been used in the project you are a memebr of ::

    du -hd 1 ./ 

Shows how much data you store in each subfolder (depth 1) ::

    du --inodes -hd 1 ./ 

Shows how many files you store in each subfolder (depth 1) ::

Different ways of checking the queue::

    squeue -A naiss2024-1-3
    squeue --me
    squeue --reservation lsda  -o"%.7i %.9P %.8j %.8u %.2t %.10M %.6D %C %.11l"
    squeue --format="%.18i %.9P %.30j %.8u %.8T %.10M %.9l %.6D %R" --me


Change permissions for specific user for a certain folder ::

   setfacl -R -m u:x_user:rx folder/


