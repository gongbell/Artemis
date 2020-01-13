# Artemis

An extended Ethereum smart contract verification tool to detect vulnerabilities including Freezing Ether, Block information dependency, Gasless send and Dangerous delegatecall. Artemis is based on Oyente.(https://github.com/melonproject/oyente)

Quick Start

A container with the dependencies set up can be found here. 
Solc version management depends on solc-select. (https://github.com/crytic/solc-select.)

To open the container, install docker and run:

$ docker import artemis.tar artemis/artemis

$ docker run -t -i artemis/artemis /bin/bash

$ export PATH=/root/.solc-select:$PATH

$ solc use 0.4.11(Tested version)

$ cd artemis/artemis

$ python artemis.py -s <contract filename> -b
  
Full installation

Install the following dependencies

solc

$ sudo add-apt-repository ppa:ethereum/ethereum

$ sudo apt-get update

$ sudo apt-get install solc

evm from go-ethereum

1.https://geth.ethereum.org/downloads/ or

2.By PPA if your using Ubuntu

$ sudo apt-get install software-properties-common

$ sudo add-apt-repository -y ppa:ethereum/ethereum

$ sudo apt-get update

$ sudo apt-get install ethereum

z3 Theorem Prover version 4.5.0.

Download the source code of version z3-4.5.0

Install z3 using Python bindings

$ python scripts/mk_make.py --python

$ cd build

$ make

$ sudo make install

Requests library

pip install requests

web3 library

pip install web3

Evaluating Ethereum Contracts

#evaluate a local solidity contract

python artemis.py -s <contract filename>

#evaluate a local evm contract

python artemis.py -s <contract filename> -b
