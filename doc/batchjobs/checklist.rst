.. _checklist:

Running jobs on Tetralith
=====================

Checklist
+++++++++++++++++++++++

If you develop your own codes/scripts or would like to increase the allocated resources for an existing code, please work through this checklist before submitting your production runs or a large number of jobs.

1. **Is your code/script parallelised?** No -> Use one core: **n 1 not N 1**


2. If yes -> How is it parallelised?

   **Can your code make use of more than one node?** Check by first doing short test jobs.

   * Does the job finish quicker when more resources are allocated?
   * Does the job make use of all the allocated resources? Use e.g. seff:

   .. code-block:: text
       :emphasize-lines: 11
   
       $seff job_id_of_test_job
   
       Example output
       Job ID: 26294158
       Cluster: tetralith
       User/Group: x_alewi/x_alewi
       State: COMPLETED (exit code 0)
       Nodes: 4
       Cores per node: 32
       CPU Utilized: 474-08:22:07
       CPU Efficiency: 99.60% of 476-05:58:24 core-walltime
       Job Wall-clock time: 3-17:17:48
       Memory Utilized: 166.25 GB (estimated maximum)
       Memory Efficiency: 0.00% of 0.00 MB (0.00 MB/node)
   
   
   What is the difference between the core-walltime and Job Wall-clock time here? The Wall time is how long time it takes for your job to finish, in “real time”. The core-walltime (or total number of core hours used for the job) is the wall time multiplied with the number of allocated cores, i.e. 34*4 times 3 days, 17 hours, 17 minutes and 48 seconds in the example above.
   
   Is the code parallelised with MPI, OpenMP or simply running independent processes in parallel? If you are not sure how to allocate the right resources, ask for help.


3. **How does your job scale?** The performance will decrease with increasing number of resources (communication overhead) and there is always a performance-walltime tradeoff. How important is it to have your job finish more quickly? Is the decreased job time worth the extra core hour consumption?

   Example scalability test. Blue line shows the walltime for the job depending on the number of cores used. The red line shows ideal scaling. The difference between the blue and red lines represents communication overhead/blocking etc. I would use 32 cores for this job based on the performance test. 

.. image:: /images/scale.png
  :width: 600
  :alt: Missing image file

   The maximum wall time on Tetralith is 7 days. If your job cannot finish within 7 days, there are workarounds, but these should in general be avoided*. If your jobs need more than seven days of wall time, please ask for help to set up a plan for how to manage your jobs.



4. Is your resource usage reasonable? The answer is usually “It depends”. A rule of thumb is: 

  **“Avoid using resources in a way that blocks other users from using them or prevents them from working efficiently”.** 

   What this means depends on the current workload in the project. Please always check the queue status and current usage before submitting a job



   Check the queue of the project::
       $ squeue -A snic2022-1-1

   Check the recent usage
   .. code-block:: text
       :emphasize-lines: 4, 7

       $ projinfo
       Principal Investigator (PI):   Qiong Zhang    
       Slurm account:             	snic2022-1-1   
       Current core time allocation:  2000000 h/month
       Consumed compute resource time during the last 30 days:

       Total:                                	2001774.68


   Keep checking the queue and core time consumption as your jobs run. 



