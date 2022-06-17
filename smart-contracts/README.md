# Smart Contracts

by Jonathan (nviso)

based on a talk Jonathan gave on smart contract security.

## blockchain

* first block called "genesis"
* next block contains revious hash

## smart contract

* program stored on the blockchain = immutable program
* runs e.g. on the ethereum VM
* not really a contract, just code

## smart contract example: escrow

* alice and bob want to do business, don't trust each other, they need an escrow, notary, laywer?
* bob wants to sell an nft to alice
* alice sends crypotcurrency to the smart contract
* bob sends nft ownership to alice
* contract pays bob

## decentralization and consensus

The Byzantine Generals problem

* proof of work -- high energy consumption
* proof of stake -- ethereum: 33 ether ~ 33.000 € -- right to validation proportinal to investment
* proof of authority -- validators earn the right to validate -- in private blockchains

## platforms

* ethereum: 14-27 transactions per second - not enought for somthing like credit card processing
* polkadot
* solana
* hyperledger - linux fuondation, ibm, jp morgan, cisco, intel, focus on data protectino, private, 1000 transaction per second
* steallar

## dapps

web client
* https://metamask.io/
* https://web3js.readthedocs.io/en/v1.7.3/

backend api
* for stuff that you dont want in the public in the contract

smart contract


## ethereum blockchain

* while bitcoin blockchain ist purly a list of transaction
* ethereum blockchain keeps track of the state of accounts



## write and deploy contract in Solidity

* solidity is the language of the contract
* compile to byte code (binary) and interface defintion (ABI)
* deploy to the ethereum network


## two types of accounts

externally  (by a person) owned account

* has an ether balance
* can send transaction
* secured by a private key

contract account

* has code


## security issues

* is this contract trying to rip people off?
* are people able to rip this contract off?

if you own 51% of the nodes you own the blockchain.

its feasable in etherium, 8 million € ?

## the bug that led to the split in ethereum

https://www.heise.de/news/Der-Hack-der-Ethereum-spaltete-DAO-Angreifer-angeblich-enttarnt-6517632.html

[Smart Contract Weakness Classification and Test Cases](https://swcregistry.io/)

remix.ethereum.org

mythx.io

trufflesuite.com + ganache

tokenized assets

