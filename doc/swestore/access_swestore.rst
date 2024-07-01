.. _access_swestore:

Working with data on Swestore from Tetralith
====================

Access methods
++++++++++++++++++++

The Swestore `documentation <https://docs.swestore.se/>`_ describes several protocols for acessing data on Swestore. Here is a guide how to work with data on Swestore using rclone from Tetralith. Rclone is available on log in nodes as well as on compute nodes on Tetralith. The full rclone documentation can be found `here <https://rclone.org/>`_.


Browsing data on Swestore
+++++++++++++++++++

It is possible to browse the Swestore storage through a web-page interface: `<https://webdav.swestore.se/snic/bolinc/>`_. Data can also be downloaded from this web page. Username and :ref:`password <swestore_login>` is required for access.


Setting up rclone for Swestore
+++++++++++++++++++

Instructions for how to configure rclone for Swestore con be found on the Swestore documentation `page <https://docs.swestore.se/using/rclone/#configuration>`_. Certificates are not needed, so follow the instructions for *Username/Password* authentiction.


Basic rclone usage
+++++++++++++++++++++++++++++++

List directories

.. code-block:: text

    rclone lsd swestore:/snic/bolinc

Copy directories to Swestore

.. code-block:: text

    rclone copy -P /path/to/src swestore:/snic/bolinc/DESTINATION_DIRECTORY/src


Copy directories from Swestore

.. code-block:: text

    rclone copy -P swestore:/snic/bolinc/SOURCE_DIRECTORY/src /path/to/src
   

