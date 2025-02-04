# VeBetterDAO Smart Contracts 🌟

                                     #######
                                ################
                              ####################
                            ###########   #########
                           #########      #########
         #######          #########       #########
         #########       #########      ##########
          ##########     ########     ####################
           ##########   #########  #########################
             ################### ############################
              #################  ##########          ########
                ##############      ###              ########
                 ############                       #########
                   ##########                     ##########
                    ########                    ###########
                      ###                    ############
                                         ##############
                                   #################
                                  ##############
                                  #########

[![codecov](https://codecov.io/gh/vechain/vebetterdao-contracts/graph/badge.svg?token=3OMYFKUMS9)](https://app.codecov.io/gh/vechain/vebetterdao-contracts)

Welcome to the VeBetterDAO Smart Contracts repository! This open-source repository houses the smart contracts powering the decentralized VeBetterDAO on the VeChain Thor blockchain. Dive into a world of transparent and auditable governance mechanisms, leveraging Solidity, Hardhat, and more to ensure robust decentralized operations.

The complete documentation for the VeBetterDAO and the contracts can be found [here](https://docs.vebetterdao.org).

## Mainnet contract addresses

```
  "B3TR": "0x5ef79995FE8a89e0812330E4378eB2660ceDe699",
  "B3TRGovernor": "0x1c65C25fABe2fc1bCb82f253fA0C916a322f777C",
  "Emissions": "0xDf94739bd169C84fe6478D8420Bb807F1f47b135",
  "GalaxyMember": "0x93B8cD34A7Fc4f53271b9011161F7A2B5fEA9D1F",
  "TimeLock": "0x7B7EaF620d88E38782c6491D7Ce0B8D8cF3227e4",
  "Treasury": "0xD5903BCc66e439c753e525F8AF2FeC7be2429593",
  "VOT3": "0x76Ca782B59C74d088C7D2Cce2f211BC00836c602",
  "VoterRewards": "0x838A33AF756a6366f93e201423E1425f67eC0Fa7",
  "X2EarnApps": "0x8392B7CCc763dB03b47afcD8E8f5e24F9cf0554D",
  "X2EarnRewardsPool": "0x6Bee7DDab6c99d5B2Af0554EaEA484CE18F52631",
  "XAllocationPool": "0x4191776F05f4bE4848d3f4d587345078B439C7d3",
  "XAllocationVoting": "0x89A00Bb0947a30FF95BEeF77a66AEdE3842Fe5B7"
```

## Audit

The VeBetterDAO smart contracts have undergone a comprehensive audit by [Hacken](https://hacken.io/). The audit report (`Hacken_Vechain Foundation_[SCA] VeChain _ VeBetter DAO _ May2024_P-2024-304_1_20240621 16_17`) can be found in the root of the repo.

## Requirements

Before contributing or deploying, ensure your environment meets the following specifications:

- **Node.js (v20 or later):** [Download Node.js](https://nodejs.org/en/download/package-manager) 📥
- **Docker:** [Install Docker](https://docs.docker.com/get-docker/) for running isolated contract environments 🐳
- **Hardhat:** Essential for smart contract compilation and deployment. [Start with Hardhat](https://hardhat.org/getting-started/) ⛑️

## Repository Structure

### Contracts (contracts/) 📜

Core smart contracts written in Solidity. Managed with Hardhat, these contracts are ready for deployment on the VeChain Thor blockchain.

### Artifacts (artifacts/) 🏺

Automatically generated contract artifacts post-compilation. Contains ABI and contract bytecode.

### TypeChain Types (typechain-types/) 📚

TypeScript typings for smart contracts, generated to enhance developer experience by providing strong typing for contract interactions.

## Environment Setup ⚙️

Set up your environment to integrate smoothly with the blockchain:

- **MNEMONIC:** Store the mnemonic for the deploying wallet in a `.env` file at the root to maintain security and ease of use.

## Getting Started 🏁

Clone the repository and install dependencies with ease:

```bash
yarn install # Run this at the root level of the project
```

## Compilation and Testing 🛠️

Compile contracts and generate necessary artifacts and types:

```bash
yarn compile
```

### Testing on Hardhat Network

```bash
yarn test:hardhat
```

### Testing on Thor Solo Network

```bash
yarn test:thor-solo
```

### Code coverage

You can generate code coverage reports using the following command:

```bash
yarn test:coverage:solidity
```

A folder named `coverage` will be created in the root directory with the coverage report. Open `index.html` in your browser to view the report.

Additionally a report is generated each time a PR is merged on main and can be found [here](https://app.codecov.io/gh/vechain/vebetterdao-contracts).

### Slither

Note that slither does not seem to be working with the repo as-is, resulting in an enum type not found error:

```bash
slither.solc_parsing.exceptions.ParsingError: Type not found struct Checkpoints.Trace208
```

# Disclaimer

This repository is for educational and demonstration purposes. The maintainers are not liable for any misuse or faults within the code.
