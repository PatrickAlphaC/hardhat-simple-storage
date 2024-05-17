# Update: Head to Cyfrin Updraft

> **ℹ️ Important:** This repo is no longer maintained; we invite all people learning Solidity to head to [Cyfrin Updraft](https://updraft.cyfrin.io/)! The 100% free #1 smart contract education platform on earth. Developed with love by Patrick & Cyfrin <3

# Hardhat Simple Storage

- [Hardhat Simple Storage](#hardhat-simple-storage)
- [Getting Started](#getting-started)
  - [Requirements](#requirements)
  - [Quickstart](#quickstart)
  - [Typescript](#typescript)
- [Useage](#useage)
  - [Testing](#testing)
    - [Test Coverage](#test-coverage)
  - [Estimate gas](#estimate-gas)
  - [Local Deployment](#local-deployment)
    - [Important localhost note](#important-localhost-note)
  - [Deployment to a testnet or mainnet](#deployment-to-a-testnet-or-mainnet)
    - [Verify on etherscan](#verify-on-etherscan)
- [Linting](#linting)
- [Thank you!](#thank-you)


# Getting Started

## Requirements

- [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
  - You'll know you did it right if you can run `git --version` and you see a response like `git version x.x.x`
- [Nodejs & npx](https://nodejs.org/en/)
  - You'll know you've installed nodejs right if you can run:
    - `node --version`
    - And get an ouput like:
    - `vx.x.x`
  - You'll know you've installed npx right if you can run:
    - `npx --version`
    - And get an ouput like:
    - `x.x.x`
    - You might need to install it with npm
- [Yarn](https://classic.yarnpkg.com/lang/en/docs/install/) instead of `npm`
  - You'll know you've installed yarn right if you can run:
    - `yarn --version`
    - And get an output like:
    - `x.x.x`
    - You might need to install it with npm

## Quickstart

```
git clone https://github.com/PatrickAlphaC/hardhat-simple-storage-fcc
cd hardhat-simple-storage-fcc
yarn 
```

## Typescript

For the typescript edition, run:

```
git checkout typescript
```


# Useage

Deploy:

```
npx hardhat run scripts/deploy.js
```

## Testing

```
npx hardhat test
```

### Test Coverage

```
npx hardhat coverage
```

## Estimate gas

You can estimate how much gas things cost by running:

```
npx hardhat test
```

And you'll see and output file called `gas-report.txt`

## Local Deployment 

If you'd like to run your own local hardhat network, you can run:

```
npx hardhat node
```

This will also deploy your `SimpleStorage.sol` contract. 

And you should see transactions happen in your terminal that is running `npx hardhat node`

### Important localhost note

If you use metamask with a local network, everytime you shut down your node, you'll need to reset your account. Settings -> Advanced -> Reset account. Don't do this with a metamask you have real funds in. And maybe don't do this if you're a little confused by this. 

## Deployment to a testnet or mainnet

1. Setup environment variabltes

You'll want to set your `KOVAN_RPC_URL` and `PRIVATE_KEY` as environment variables. You can add them to a `.env` file, similar to what you see in `.env.example`.

- `PRIVATE_KEY`: The private key of your account (like from [metamask](https://metamask.io/)). **NOTE:** FOR DEVELOPMENT, PLEASE USE A KEY THAT DOESN'T HAVE ANY REAL FUNDS ASSOCIATED WITH IT.
  - You can [learn how to export it here](https://metamask.zendesk.com/hc/en-us/articles/360015289632-How-to-Export-an-Account-Private-Key).
- `KOVAN_RPC_URL`: This is url of the kovan testnet node you're working with. You can get setup with one for free from [Alchemy](https://alchemy.com/?a=673c802981)

2. Get testnet ETH

Head over to [faucets.chain.link](https://faucets.chain.link/) and get some tesnet ETH. You should see the ETH show up in your metamask.

3. Deploy

```
npx hardhat run scripts/deploy.py --network kovan
```

### Verify on etherscan

If you deploy to a testnet or mainnet, you can verify it if you get an [API Key](https://etherscan.io/myapikey) from Etherscan and set it as an environemnt variable named `ETHERSCAN_API_KEY`. You can pop it into your `.env` file as seen in the `.env.example`.

In it's current state, if you have your api key set, it will auto verify kovan contracts!

However, you can manual verify with:

```
npx hardhat verify --constructor-args arguments.js DEPLOYED_CONTRACT_ADDRESS
```

# Linting

To check linting / code formatting:
```
yarn lint
```
or, to fix: 
```
yarn lint:fix
```

# Thank you!

If you appreciated this, feel free to follow me or donate!

ETH/Polygon/Avalanche/etc Address: 0x9680201d9c93d65a3603d2088d125e955c73BD65

[![Patrick Collins Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/PatrickAlphaC)
[![Patrick Collins YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/channel/UCn-3f8tw_E1jZvhuHatROwA)
[![Patrick Collins Linkedin](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/patrickalphac/)
[![Patrick Collins Medium](https://img.shields.io/badge/Medium-000000?style=for-the-badge&logo=medium&logoColor=white)](https://medium.com/@patrick.collins_58673/)
