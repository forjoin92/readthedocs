Mining
======

--------------

CPU Mining
----------

Currently, Seele provides CPU Miner.

**Attention**\ ，If you want to do mining on Seele，please make sure you
are running the Seele Node on the Main-Net，and has to be run as full
node.If you are not familiar with Seele，please read `Getting Started
With Seele <Getting-Started-With-Seele.html>`__.

Start mining on Seele Node
~~~~~~~~~~~~~~~~~~~~~~~~~~

You could start mining at the same time when Seele Node is
starting，\ `Setting Up a
Node <Getting-Started-With-Seele.html#setting-up-a-node>`__ will help
you on how to build a Node and start Seele Node.

Seele Node provides the ``--miner, -m`` command line parameter to
specify whether to start mining when Node starts. The default is to
start. If you don’t want to mine, you can use ``--miner stop`` when
starting Node. The Seele Node also provides the ``--threads`` command
line argument to set the number of threads used by the Miner started by
Node.

Example
^^^^^^^

A configuration file is required at start of Seele Node, and the format
of the configuration file is referenced `configpath <#configpath>`__\ .

configpath
''''''''''

.. code:: sh

   {
     "basic":{
       "name": "seele node1",
       "version": "1.0",
       "dataDir": "node1",
       "address": "0.0.0.0:8027",
       "coinbase": "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21",
       "algorithm": "sha256"
     },
     "p2p": {
       "privateKey": "0xf65e40c6809643b25ce4df33153da2f3338876f181f83d2281c6ac4a987b1479",
       "staticNodes": [],
       "address": "0.0.0.0:8057",
       "networkID": "seele"
     },
     "log": {
       "isDebug": true,
       "printLog": true
     },
     "httpServer": {
       "address": "0.0.0.0:8037",
       "crossorigins": [
         "*"
       ],
       "whiteHost": [
         "*"
       ]
     },
     "wsserver": {
       "address": "0.0.0.0:8047",
       "crossorigins": [
         "*"
       ]
     },
     "metrics": {
       "address": "0.0.0.0:8087",
       "duration": 10,
       "database": "influxdb",
       "username": "test",
       "password": "test123"
     },
     "genesis": {
       "difficult":8000000,
       "shard":1,
       "timestamp":1539742676
     }
   }

// Start mining by default when starting Seele Node

.. code:: sh

   node start -c configpath

// Start mining when starting Seele Node, and set the number of threads
used by Miner to 2

.. code:: js

   node start -c configpath --threads 2

// Mining does not start when starting Seele Node

.. code:: js

   node start -c configpath --miner stop

Start mining with Seele Full Client
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you already have a Seele full node, you can use the full node client
to start and manage your Node Miner `Create a Full Node
Client <Getting-Started-With-Seele.html#create-a-full-node-client>`__
will help you on how to acquire a full client node.

.. _example-1:

Example
^^^^^^^

Client starts mining：

.. code:: js

   client miner start

   true

Client starts mining and sets the number of Miner threads to 2：

.. code:: js

   client miner start --threads 2

   true

Client stops mining：

.. code:: js

   client miner stop

   true

Get the Seele Node Miner running status：

.. code:: js

   client miner status

   "Running"

   or

   "Stopped"

Get Seele Node Miner Coinbase:

.. code:: js

   client miner getcoinbase

   "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21"

Sets Seele Node Miner Coinbase:

.. code:: js

   client miner setcoinbase "0x4c10f2cd2159bb432094e3be7e17904c2b4aeb21"

   true

Sets Seele Node Miner thread to 2:

.. code:: js

   client miner setthreads --threads 2

   true

Get Seele Node Miner Engine Information:

.. code:: js

   client miner getengineinfo

   {
       "hashrate": 495812.2433994204,
       "threads": 1
   }

Other Mining
------------

Other Mining is currently under development.
