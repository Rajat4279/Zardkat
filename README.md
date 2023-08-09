# ZK Circuit

This program involves a simple logical gate circuit that generates a proof using SnarkJS, and deploys a solidity verifier. All this is done in hardhat. [zardkat](https://github.com/gmchad/zardkat), a light template built on top of hardhat-circom, is used to implement the entire zkSNARK flow in hardhat.
## Description
The circuit in the circom programming language implements the following logical gate:

![logical gate](https://authoring.metacrafters.io/assets/cms/Assessment_b05f6ed658.png?updated_at=2023-02-24T00:00:37.278Z)

In the code, "a" and "b" are the input signals, "x" and "y" are the intermediary signals, which are passed into the OR gate to get the final output signal "q".
## Getting Started

1. Clone the repository:

```

```

2. Install the dependencies :

```
cd  zardkat
npm i
```

3. Generate the out file with circuit intermediaries and generate the ZKCircuitVerifier.sol contract

```
npx hardhat circom
```

4. Prove and Deploy
```
npx hardhat run scripts/deploy.ts 
```

This script does 4 things:

1. Deploys the ZKCircuitVerifier.sol contract
2. Generates a proof from circuit intermediaries with generateProof()
3. Generates calldata with generateCallData()
4. Calls verifyProof() on the verifier contract with calldata
With the two commands you can compile a ZKP, generate a proof, deploy a verifier, and verify the proof!


## Technologies Used 
- Circom - Circom is a zkSNARK framework for compiling zero-knowledge circuits. It comes with its own domain specific language (DSL) for writing circuits, and tools to compile those circuits into artifacts.
- SnarkJS - This is a JavaScript and Pure Web Assembly implementation of zkSNARK and PLONK schemes
- MetaMask - Wallet and gateway to Ethereum blockchain  
- ethers.js - Library for interacting with Ethereum smart contracts  
- Hardhat - Development environment and task runner for building, testing, and deploying smart contracts on Ethereum and other blockchain platforms
## Authors
- Rajat
