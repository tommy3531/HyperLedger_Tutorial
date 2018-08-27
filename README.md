# Hyperledger

Is a tool kit that makes building business network with blockchain easier. 

## Composer

Enables developers to quickly create blockchain solutions, rest APIs that expose the blockchain logic to web or mobile

Components - Composer-cli, rest-server, web playground

links: https://hyperledger.github.io/composer/v0.19/introduction/solution-architecture


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


