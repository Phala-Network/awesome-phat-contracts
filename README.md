# Awesome Phat Contracts [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
<p align="center">
  <a href="https://phala.network/">
    <img alt="Phala Network" src="./assets/PhalaLogo.png">
  </a>
</p>

> A curated list of awesome projects and resources relating to Phala's Phat Contracts.
 
[Phat Contract](https://wiki.phala.network/en-us/general/development/fat-contract/) is the programming model adopted by Phala Network. Phat Contract is NOT a smart contract. Instead, it aims to provide the rich features that ordinary smart contracts cannot offer, including:

- CPU extensive computation: exclusive off-chain execution at the full CPU speed
- Network access: the ability to send the HTTP requests
- Low latency: non-consensus-sensitive operations may not hit the blockchain at all, removing the block latency
- Strong consistency: consensus-sensitive operations remain globally consistent
- Confidentiality: contract state is hidden by default unless you specifically expose it via the read call

Phat Contract is 100% compatible with Substrate’s `pallet-contracts`. It fully supports the unmodified ink! smart contracts. Therefore, you can still stick to your favorite toolchain including `cargo-contract`, `@polkadot/contract-api`, and the Polkadot.js Extension.

## Contents
- [Resources](#resources)
- [Past Hackathon dApps](#past-hackathon-dapps)
- [Phat Contract Examples](#phat-contract-examples)
- [Ink Smart Contract Examples](#ink-smart-contract-examples)


## Resources
- Rust Crates for `pink`
  - [Storage Services](https://wiki.phala.network/en-us/build/stateless/rust-crates/#use-storage-services) 
    - [`pink-s3`](https://crates.io/crates/pink-s3) - Simple pure Rust AWS S3 Client for Phala Network's `pink` environment. Supports S3-API for [4Everland](https://www.4everland.org/bucket/) to connect to Arweave, Filecoin, Storj, and AWS S3.
  - [Cross-Chain Operations](https://wiki.phala.network/en-us/build/stateless/rust-crates/#cross-chain-operations)
    - [`pink-web3`](https://crates.io/crates/pink-web3) - provides the basic cross-chain operation support for EVM-compatible chains.
    - [`pink-subrpc`](https://crates.io/crates/pink-subrpc) - provides the basic support for Substrate-based chains.
    - [`pink-kv-session`](https://crates.io/crates/pink-kv-session) - KV session primitives for phat off-chain rollup.
- Pink Extension
  - [Pink Extension Functions](https://wiki.phala.network/en-us/build/stateless/pink-extension/) - All the unique capabilities of Phat Contract are implemented in [pink-extension](https://github.com/Phala-Network/phala-blockchain/tree/master/crates/pink).
- Learning
  - [Phat Contract's Tutorial Wiki](https://wiki.phala.network/en-us/build/developer/fat-contract-tutorial/) - tutorial to demonstrate how to use Phat Contract’s HTTP request capability to associate a Phala account with a Github user. For the video tutorial checkout [Phala Phat Contract's Workshop](https://www.youtube.com/watch?v=B7fUwRxelu4&t=1963s).
  - [Frontend SDK](https://github.com/Phala-Network/js-sdk) - frontend SDK for building UI for Phala Phat Contracts.
  - [Ink! Smart Contracts Docs](https://ink.substrate.io/) - ink! is an eDSL to write smart contracts in Rust for blockchains built on the Substrate framework. ink! contracts are compiled to WebAssembly.
  - [Awesome Ink!](https://github.com/paritytech/awesome-ink) - A curated list of awesome projects related to Parity's ink!.
- Articles/Blogs/Papers
  - [Substrate Off-Chain Workers](https://www.parity.io/blog/substrate-off-chain-workers-secure-and-efficient-computing-intensive-tasks/) - An post on secure and efficient computing-intensive tasks written by Phil Lucsok in 2019.
  - [Phala's Phat Contract](https://medium.com/supercolony/fat-contract-introduce-off-chain-computation-to-smart-contract-d44dc8afb141) - A Medium post about the introduction of off-chain computation to smart contracts written by Phala's Lead Researcher Dr. Shelven Zhou.
  - [Off-chaining Models and Approaches to Off-chain Computations](https://www.ise.tu-berlin.de/fileadmin/fg308/publications/2018/Off-chaining_Models_and_Approaches_to_Off-chain_Computations.pdf) - A paper written by Jacob Eberhardt & Jonathan Heiss describing off-chaining models using verifiable off-chain computation (**zkSNARKS**, **Bulletproofs**, **zkSTARKS**), enclave based off-chain computation (**TEEs**), secure multiparty computation based off-chaining (**sMPC**) & incentive-driven off-chain computing (**IOC**).
- Tools
  - [Phala Contract's UI](https://phat.phala.network) - UI frontend to deploy Phat Contracts.
  - [Phala Swanky Integration](https://github.com/AstarNetwork/swanky-plugin-phala) - Phala Swanky integration for an all-in-one development environment for WASM ink-based Phat Contracts.
  - [DevPHAse](https://github.com/l00k/devphase) - Run a Phala local testnet and compile/test Phat Contracts in a development environment.
- Service Limits
  - [Service Limits Table](https://wiki.phala.network/en-us/build/support/resource-limits/) - service limits for Phat Contracts and SideVM.

## Past Hackathon dApps
- [PhaPass](https://github.com/Phala-Network/Encode-Hackathon-2021/issues/12) - a password manager on Phala
- [Darkpool DEX](https://github.com/Phala-Network/Encode-Hackathon-2021/issues/16) - a proof-of-concept Darkpool Decentralized Exchange as a dApp/smart contract on top of Phala.
- [RMRK Ghost Auction](https://github.com/Phala-Network/Encode-Hackathon-2021/issues/19) - a simple ghost auction that would allow RMRK NFT artists to run automated auctions while not available on Singular using HTTP requests on Phala Phat Contracts.
- [SecretMD](https://github.com/Phala-Network/Encode-Hackathon-2021/issues/20) - a rich markdown editor which allows users to store and share any plain markdown file onto a distributed and confidential Phala blockchain in Polkadot ecosystem.
- [Phat 2FA](https://github.com/Phala-Network/amsterDOT-2022/issues/12) - an application achieves two-factor authentication on chain, without leaking any sensitive data.
- [Privacy Preserving Voting](https://github.com/Phala-Network/amsterDOT-2022/issues/10) - a simple account based voting mechanism using Phat Contracts.

## Phat Contract Examples
- [Sub0 2022 Oracale & Off-Chain Rollup Workshop](https://github.com/Phala-Network/phat-offchain-rollup/tree/sub0-workshop) - an upgrade from the Oracle Workshop that implements the off-chain rollup pallet in the Phala testnet chain for the Phat Contract to respond with price feed information from the Phat Contracts to the Phala testnet chain.
- [Oracle Workshop](https://github.com/Phala-Network/oracle-workshop) - an extensive workshop demonstrating how to write an Oracle with Phat Contracts.
- [Phat Contract Examples](https://github.com/Phala-Network/fat-contract-examples) - boilerplate examples of various Phat Contracts.
- [Phat Storage](https://github.com/christopherfkk/fat-contract-s3-sync) - how to connect Phala's Phat Contract to external storage services, both centralized (Amazon s3) and decentralized (Arweave/Filecoin through 4everland, Storj, Filebase).
- [ETH Holder](https://github.com/www222fff/oracle-workshop/tree/master/eth_holder) - derive an ETH ECDSA account in the Phat Contract then fund the account w/ ETH and send a raw transaction to a configured RPC Node with the `eth_sendRawTransaction` RPC method.
- [Phat RPC](https://github.com/HashWarlock/phat-contract-examples/tree/master/examples/phat-rpc) - a Phat Contract that can interact with OnFinality RPC nodes through HTTPS requests.
- [Secret File](https://github.com/shelvenzhou/secret-file) - secret file implementation using Phat Contracts.
- [Github Attestation](https://github.com/Phala-Network/fat-contract-workshop) - a workshop demonstrating how to write a Phat Contract with its HTTP request capability on Phala.
- [X-Chain HTTP Request: Subgraph NounsDAO](https://github.com/HashWarlock/phat-contract-examples/tree/master/examples/subgraph-nouns) - demonstrate how to make a HTTPS request to an indexing service Subgraph to query information about the NounsDAO collection in a Phat Contract.
- [Roshambo](https://github.com/HashWarlock/phat-contract-examples/tree/master/examples/roshambo) - a game of Roshambo (Rock, Paper, Scissors) in a Phat Contract.

## Ink Smart Contract Examples
- [Parity's Ink!](https://github.com/paritytech/ink) - Parity's ink! to write WASM smart contracts.
- [Astar's Swanky CLI](https://github.com/AstarNetwork/swanky-cli) - The all-in-one developer environment for Parity WASM smart contracts!
- [OpenBrush Library](https://github.com/Supercolony-net/openbrush-contracts) - OpenBrush is a library for smart contract development on ink!
- [Candle Auction](https://github.com/agryaznov/candle-auction-ink) - an Ink! smart contract implementing a candle auction logic.
- [Dead Man Switch](https://github.com/lovesh/dead_man_switch_substrate_ink) - a dead man's switch written using ink! smart contracts.
- [Nested Structs Example](https://github.com/czyczk/exp-ink-struct) - a boilerplate example of using nested structs for ink! smart contracts.
