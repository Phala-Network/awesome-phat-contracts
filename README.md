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

## Resources
- Learning
  - [Fat Contract's Tutorial Wiki](https://wiki.phala.network/en-us/build/developer/fat-contract-tutorial/) - tutorial to demonstrate how to use Fat Contract’s HTTP request capability to associate a Phala account with a Github user. For the video tutorial checkout [Phala Fat Contract's Workshop](https://www.youtube.com/watch?v=B7fUwRxelu4&t=1963s).
  - [Ink! Smart Contracts Docs](https://ink.substrate.io/) - ink! is an eDSL to write smart contracts in Rust for blockchains built on the Substrate framework. ink! contracts are compiled to WebAssembly.
  - [Awesome Ink!](https://github.com/paritytech/awesome-ink) - A curated list of awesome projects related to Parity's ink!.
