# Hyperledger

Is a tool kit that makes building business network with blockchain easier. 

## Composer

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


### When should I user Composer?

If you need to create a Business network you should user composer.  A business network is comprised of model, script, access control and query file.  Package up the business network and export it as a an archive(.bna file) ready to deploy

### What is the model, script, access control and query file

1. Model.cto
    - Contains definitions of each class of asset, transaction, participants and events

2. logic.js
    - Contains defintions of how a transaction should happen.

3. permission.acl
    - control who has access to what

4. Query file


### What is a Hyperledger Fabric Model

    - Assets- anything of value that can be represented digitially

    - Chaincode - Defining assests, transaction instructions for modifying assets. Execution results in a set of key-value writes that can be submitted to the netwrok and applied to the ledger on all peers. ??? 

    - Ledger Features - immutable, encode transactions ???

    - Privacy - Channels enable private transactions

    - Security & Membership Services - Permissioned membership provides a trusted blockchain network.

    - Consensus - Pluggable

### What are all the components of a network?

    1. Ledgers - one per channel
    2. smart contracts - chaincode
    3. peer nodes
    4. ordering services
    5. channels
    6. Fabric Certification Authorities

    


