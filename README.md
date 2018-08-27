# Blockchain

Is a distributed ledger that records all transactions that take place on the network.  It is decentralized, there is not a centeral authority all participants on the network work together to maintain the integrity of the data on the network.

Once a transaction is added to the ledger it becomes immutable which ensures the data has not changed.  This is why blockchains are described as systems of proof.

### Blockchain Smart Contracts

Consist of functions that can be used to provide controll access to the ledger.  Contain business logic to track assets and how assets are transfered from once participant to the other.  

### Blockchain Consensus

The process of keeping the ledger transactions synchronized across the network to ensure the that the ledgers update only when the transactions are approved by appropriate participants, and that when ledgers do update, they update with the same transactions in the same order.

------------------------------------------------------------------------

# Hyperledger Fabric

Key Terms - Private / Permissioned, Membership Service Provider (MSP),channels, world state, transaction logs, chaincode, consensus, 

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

    


