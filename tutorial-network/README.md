# Project Structure

    1. angualr-app
    2. features
    3. lib
    4. models
    5. test
    6. networkadmin.card
    7. package.json
    8. permission.acl
    9. tutorial-network@0.0.1.bna

# Start Dev Environment

    1. composer-rest-server - locahost:3000
    2. composer playground
    3. npm start - localhost:42000






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



