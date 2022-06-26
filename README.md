# Awesome Fat Contracts [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
<p align="center">
  <a href="https://phala.network/">
    <img alt="Phala Network" src="./assets/PhalaLogo.png">
  </a>
</p>

> A curated list of awesome projects and resources relating to Phala's Fat Contracts.
 
[Fat Contract](https://wiki.phala.network/en-us/general/development/fat-contract/) is the programming model adopted by Phala Network. Fat Contract is NOT a smart contract. Instead, it aims to provide the rich features that ordinary smart contracts cannot offer, including:

- CPU extensive computation: exclusive off-chain execution at the full CPU speed
- Network access: the ability to send the HTTP requests
- Low latency: non-consensus-sensitive operations may not hit the blockchain at all, removing the block latency
- Strong consistency: consensus-sensitive operations remain globally consistent
- Confidentiality: contract state is hidden by default unless you specifically expose it via the read call

Fat Contract is 100% compatible with Substrate’s `pallet-contracts`. It fully supports the unmodified ink! smart contracts. Therefore, you can still stick to your favorite toolchain including `cargo-contract`, `@polkadot/contract-api`, and the Polkadot.js Extension.

## Contents
- [Resources](#resources)
- [Past Hackathon dApps](#past-hackathon-dapps)
- [Fat Contract Examples](#fat-contract-examples)
- [Ink! Smart Contract Examples](#ink!-smart-contract-examples)

## Resources
- Learning
  - [Fat Contract's Tutorial Wiki](https://wiki.phala.network/en-us/build/developer/fat-contract-tutorial/) - tutorial to demonstrate how to use Fat Contract’s HTTP request capability to associate a Phala account with a Github user. For the video tutorial checkout [Phala Fat Contract's Workshop](https://www.youtube.com/watch?v=B7fUwRxelu4&t=1963s).
  - [Frontend SDK](https://github.com/Phala-Network/js-sdk) - frontend SDK for building UI for Phala Fat Contracts.
  - [Ink! Smart Contracts Docs](https://ink.substrate.io/) - ink! is an eDSL to write smart contracts in Rust for blockchains built on the Substrate framework. ink! contracts are compiled to WebAssembly.
  - [Awesome Ink!](https://github.com/paritytech/awesome-ink) - A curated list of awesome projects related to Parity's ink!.
- Articles/Blogs/Papers
  - [Substrate Off-Chain Workers](https://www.parity.io/blog/substrate-off-chain-workers-secure-and-efficient-computing-intensive-tasks/) - An post on secure and efficient computing-intensive tasks written by Phil Lucsok in 2019.
  - [Phala's Fat Contract](https://medium.com/supercolony/fat-contract-introduce-off-chain-computation-to-smart-contract-d44dc8afb141) - A Medium post about the introduction of off-chain computation to smart contracts written by Phala's Lead Researcher Dr. Shelven Zhou.
  - [Off-chaining Models and Approaches to Off-chain Computations](https://www.ise.tu-berlin.de/fileadmin/fg308/publications/2018/Off-chaining_Models_and_Approaches_to_Off-chain_Computations.pdf) - A paper written by Jacob Eberhardt & Jonathan Heiss describing off-chaining models using verifiable off-chain computation (**zkSNARKS**, **Bulletproofs**, **zkSTARKS**), enclave based off-chain computation (**TEEs**), secure multiparty computation based off-chaining (**sMPC**) & incentive-driven off-chain computing (**IOC**) 

## Past Hackathon dApps
- [PhaPass](https://github.com/Phala-Network/Encode-Hackathon-2021/issues/12) - a password manager on Phala
- [Darkpool DEX](https://github.com/Phala-Network/Encode-Hackathon-2021/issues/16) - a proof-of-concept Darkpool Decentralized Exchange as a dApp/smart contract on top of Phala
- [RMRK Ghost Auction](https://github.com/Phala-Network/Encode-Hackathon-2021/issues/19) - a simple ghost auction that would allow RMRK NFT artists to run automated auctions while not available on Singular using HTTP requests on Phala Fat Contracts
- [SecretMD](https://github.com/Phala-Network/Encode-Hackathon-2021/issues/20) - a rich markdown editor which allows users to store and share any plain markdown file onto a distributed and confidential Phala blockchain in Polkadot ecosystem
- [Fat 2FA](https://github.com/Phala-Network/amsterDOT-2022/issues/12) - an application achieves two-factor authentication on chain, without leaking any sensitive data
- [Privacy Preserving Voting](https://github.com/Phala-Network/amsterDOT-2022/issues/10) - a simple account based voting mechanism using Fat Contracts

## Fat Contract Examples
- [Secret File](https://github.com/shelvenzhou/secret-file) - secret file implementation using Fat Contracts
- [Github Attestation](https://github.com/Phala-Network/fat-contract-workshop) - a workshop demonstrating how to write a Fat Contract with its HTTP request capability on Phala
- [X-Chain HTTP Request: Subgraph NounsDAO](https://github.com/HashWarlock/phat-contract-examples/tree/master/examples/subgraph-nouns) - demonstrate how to make a HTTPS request to an indexing service Subgraph to query information about the NounsDAO collection in a Fat Contract
- [Roshambo](https://github.com/HashWarlock/phat-contract-examples/tree/master/examples/roshambo) - a game of Roshambo (Rock, Paper, Scissors) in a Fat Contract

## Ink! Smart Contract Examples
- [OpenBrush Library](https://github.com/Supercolony-net/openbrush-contracts) - OpenBrush is a library for smart contract development on ink!
- [Candle Auction](https://github.com/agryaznov/candle-auction-ink) - an Ink! smart contract implementing a candle auction logic
- [Dead Man Switch](https://github.com/lovesh/dead_man_switch_substrate_ink) - a dead man's switch written using ink! smart contracts
- [Nested Structs Example](https://github.com/czyczk/exp-ink-struct) - a boilerplate example of using nested structs for ink! smart contracts