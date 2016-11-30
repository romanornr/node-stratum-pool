[![BuildStatus](https://travis-ci.org/romanornr/node-stratum-pool.svg?branch=master)](https://travis-ci.org/romanornr/node-stratum-pool)
# node-stratum-pool
High performance Stratum poolserver in Node.js. One instance of this software can startup and manage multiple coin
pools, each with their own daemon and stratum port

#### Notice
This is a module for Node.js that will do nothing on its own.
The private NodeJS mining pool is written in a private github repositorythat handles stratum authentication&raw share data.
The miningpool is written in NodeJS and the backend api in Ruby. The frontend in Vuejs.
Both backend and frontend are in a private github repository,

This server was built to be more efficient and easier to setup, maintain and scale than existing stratum poolservers
which are written in python.

Features
----------------------------------
* Daemon RPC interface
* Stratum TCP socket server
* Block template / job manager
* P2P to get block notifications as peer node
* Optimized generation transaction building
* Connecting to multiple daemons for redundancy
* Process share submissions
* Session managing for purging DDoS/flood initiated zombie workers
* Auto ban IPs that are flooding with invalid shares
* __POW__ (proof-of-work) & __POS__ (proof-of-stake) support
* Transaction messages support
* Vardiff (variable difficulty / share limiter)
* When started with a coin deamon that hasn't finished syncing to the network it shows the blockchain download progress and initializes once 
synced
