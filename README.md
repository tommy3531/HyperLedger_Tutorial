# Blockchain

Is a distributed ledger that records all transactions that take place on the network.  It is decentralized, there is not a centeral authority all participants on the network work together to maintain the integrity of the data on the network.

Once a transaction is added to the ledger it becomes immutable which ensures the data has not changed.  This is why blockchains are described as systems of proof.

### Blockchain Smart Contracts

Consist of functions that can be used to provide controll access to the ledger.  Contain business logic to track assets and how assets are transfered from once participant to the other.  

### Blockchain Consensus

The process of keeping the ledger transactions synchronized across the network to ensure the that the ledgers update only when the transactions are approved by appropriate participants, and that when ledgers do update, they update with the same transactions in the same order.

# Hyperledger

Consisit of framework and modules, frameworks consist of ledger, consensu algorithm. privacy and smartcontracts.  


### What are some Hyperledger frameworks?

    1. Iroha - Caters to mobile developer uses the YAC consensu algorithm
    2. Sawtooth - Modular platform for building, deploying, and running distrubuted ledgers, can utitlize            different censnsus algorithms, by default it uses proof of elapsed time (PoET), scalability without high      energy consumption. Supports permissioned and permissionless deployments.  Network can grow nad change        consensue on the fly.
    3. Fabric - provides plug and play for membership services and consensus, channel to provide confidential        transactions.
    4. Indy - built for decentralized identity. Privacy by design
    5. Burrow - is a permissionable smart contract machine that provides a modular blockchain client with a          permissioned smart contract.
        - Major Components
            - Gateway
            - Smart contract application engine
            - Consensus Engine
            - Application blockchain interface

### What are modules and how are they used?

Moduels are used for deploying and maintaining blockchains, examining ledger data, design and extending blockchain networks.

    1. Cello - ??
    2. Explorer - ??
    3. Composer - ??
        1. Tools
            1. composer-cli
            2. rest-server
            3. yomen
            4. playground
            5. javascript
            

------------------------------------------------------------------------

# Hyperledger Fabric

Key Terms - Private / Permissioned, Membership Service Provider (MSP),channels, world state, transaction logs, chaincode, consensus. 

-----------------------------------------------------------------------

Is a blockchain project within hyperledger, it has a ledger, user smart contracts, and is a system by which particpants manager their transactions.

Fabric is private and permissioned, members of the network enroll through a trusted Membership Serivce Provider (MSP).

What makes Fabric different is that offers serveral pluggins for ledger to store mutiple data formats, consensus algorthims and MSPs. 

Is a tool kit that makes building business network with blockchain easier. 

Hyperledger fabric also offers channels, channels help to keep competitors from seeing transactions.  Channels also help with keep data private between parities.  

### Hyperledger Fabric Ledger

Has ledger subsystem comprising two components: the world state and transaction log. Each participant on the network has there own copy of the ledger.  

THe world state describes the state of the ledger at a given point in time, it is the DB of the ledger.  The transaction log records all transactions which have resulted in the current value of the world state, update history for the world state.  The ledger is a combination of the world state and transaction log history.

### Hyperledger Fabric Smart Contracts

Are written in chaincode and are invoked by an application external to the blockchain when that application needs to interact with the ledger. The chaincode interacts with the ledger the world state and not the transaction log.

### Hyperledger Fabric Consensus

# Hyperledger Fabric Functionalities

Enables developers to quickly create blockchain solutions, rest APIs that expose the blockchain logic to web or mobile. Is also adds the following functions to the network

    1. Identify Management
        - permissioned based networks, where all participants on the network must be authenticed. Access control list add extra layer of permissions through authorization of specific network operations. More control over who can have access what.

    2. Privacy and Confidentiality
        - Private channel can help with keeping transactions confidential.  Access is granted, privacy is understood by making data invisble to members not explicitly granted access to channel.

    3. Efficient Processing
        - Assigns network roles by node type. 

    4. Chaincode functionality
        - encodes logic that is invoked by transactions on the channel.

    5. Modular Design

Components - Composer-cli, rest-server, web playground

links: https://hyperledger.github.io/composer/v0.19/introduction/solution-architecture

https://hyperledger-fabric.readthedocs.io/en/release-1.2/functionalities.html

# Hyperledger Fabric Model

    - Assets- anything of value that can be represented digitially

    - Chaincode - Defining assests, transaction instructions for modifying assets. Execution results in a set of key-value writes that can be submitted to the netwrok and applied to the ledger on all peers. ??? 

    - Ledger Features - immutable, encode transactions ???

    - Privacy - Channels enable private transactions

    - Security & Membership Services - Permissioned membership provides a trusted blockchain network.

    - Consensus - Pluggable

# Hyperledger Fabric Network

    1. Ledgers - one per channel
    2. smart contracts - chaincode
    3. peer nodes
    4. ordering services
    5. channels
    6. Fabric Certification Authorities




### Creating a Business network structure

The key concept for Hyperledger composer is the business network.  It defines the DATA MODEL, TRANSACTION LOGIC and ACCESS CONTROL RULES.

To create a business network use Yeoman

    1. yo hyperledger-composer:<BUSINESS NETWORK NAME>
    2. select org.example.<BUSINESS NETWORK NAME>
    3. Select No when asked whether to generate an empty network or not

### Genrate business network archieve

    1. Navigate to directory
        1. composer archieve create -t dir -n . 

### Deploy the business network

    1. composer netwrok install --card PeerAdmin<SOMETHING> -- archieveFile <BUSINESS NETWORK NAME.bna>

### Start the business network

    1. composer network start --networkName <BUSINESS NETWORK NAME> --networkVersion<0.0.1> --networkAdmin admin --networkAdminEnrollSecrete adminpw --card PeerAdmin@<SOMETHING> --file networkadmin.card

### Import network administrator identity as a usable business network card

    1. composer card import --file networkadmin.card

### Check that the business network has been deployed

    1. composer network ping --card admin@<BUSINESS NETWORK NAME>

### Generating a REST server

    1. composer-rest-server
    2. Enter admin@<BUSINESS NETWORK NAME>
    3. never use namespaces
    4. NO dont secure API
    5. YES enable event publication
    6. NO dont enable TLS security

### Generating Application

    1. yo hyperledger-composer:angular
    2. Yes, connect to running business network
    3. package.json
    4. admin@<BUSINESS NETWORK NAME>
    5. CONNECT to an exisiting REST API
    6. locahost:3000
    7. Namespaces are not used

    


