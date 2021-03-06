
Using Postscript
----------------

Postscript Execution Order Summary
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

+---------------------------------------------------------------------------+
|                          Diskless                                         |
+----------------+-----------------+----------------------------------------+
| Stage          | Scripts         | Execute Order                          |
+================+=================+========================================+
| Install/Create | postinstall     | genimage, after packages are installed |
+----------------+-----------------+---+------------------------------------+
| Boot/Reboot    |                 | 1 | postscripts.xcatdefaults           |
|                |                 +---+------------------------------------+
|                | postscripts     | 2 | osimage                            | 
|                |                 +---+------------------------------------+
|                |                 | 3 | node                               | 
|                +-----------------+---+------------------------------------+
|                | postbootscripts | 4 | postscripts.xcatdefaults           |
|                |                 +---+------------------------------------+ 
|                |                 | 5 | osimage                            |
|                |                 +---+------------------------------------+ 
|                |                 | 6 | node                               |
+----------------+-----------------+---+------------------------------------+

.. include:: ../../../common/deployment/prepostscripts/post_script.rst
