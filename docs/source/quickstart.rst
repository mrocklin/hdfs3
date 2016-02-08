Quickstart
----------

Install ``hdfs3`` and its dependencies:

.. code-block:: bash

   $ conda install hdfs3 -c blaze

Import ``hdfs3`` and connect to the name node of an HDFS cluster:

.. code-block:: python

   >>> from hdfs3 import HDFileSystem
   >>> hdfs = HDFileSystem()

Write data to file:

.. code-block:: python

   >>> with hdfs.open('/tmp/myfile.txt', 'w') as f:
   ...     f.write(b'Hello, world!')

Read data back from file:

.. code-block:: python

   >>> with hdfs.open('/tmp/myfile.txt') as f:
   ...     print(f.read())

Interact with files on HDFS:

.. code-block:: python

   >>> hdfs.ls('/tmp')

   >>> hdfs.put('local-file.txt', '/tmp/remote-file.txt')

   >>> hdfs.cp('/tmp/remote-file.txt', '/tmp/copied-file.txt')
