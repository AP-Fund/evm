**Please note**: This repo is undergoing changes while the code is being audited and tested. For the time being we will
be making v0.x releases. Some breaking changes might occur. AP CHAIN Labs will only mark the AP CHAIN EVM repository as stable with a v1
release after the audit, key stability features and benchmarking are completed.

**Visit the official documentation for AP CHAIN EVM**: [APCHAIN.io](https://apchain.io/)

## What is AP CHAIN EVM?

AP CHAIN EVM is a plug-and-play solution that adds EVM compatibility and customizability to your AP CHAIN SDK chain. AP CHAIN EVM equips AP CHAIN chains with complete Ethereum capabilities: Solidity smart contracts, Ethereum JSON-RPC, native support for the EVM wallet/token/user experience, and access to the entire Ethereum developer ecosystem. Its precompiles and extensions allow developers to leverage modules like [IBC](https://github.com/AP CHAIN/ibc-go) with EVM and get native ERC-20 support for tokens on AP CHAIN. 

AP CHAIN EVM is customizable for your business use case, chain architecture, and performance needs.


## Integration

AP CHAIN EVM can be integrated into your existing chain
or added during the development of your upcoming chain launch
by importing AP CHAIN EVM as a go module library.

### Robust defaults

AP CHAIN EVM’s modules come out of the box with defaults that enable rapid VM deployment. Integrating all available modules into a blockchain provides:

- Exposed JSON-RPC endpoints for connectivity with EVM tooling like wallets such as [MetaMask](https://metamask.io/) and [Rabby](https://rabby.io/), and block explorers like [Blockscout](https://docs.blockscout.com/).
- EVM extensions that allow functionality that is native to AP CHAIN SDK modules to be accessible from Solidity smart contracts [Solidity](https://docs.soliditylang.org/en/v0.8.26/) smart contracts.
- Use of any IBC asset in the EVM.

All modules can be controlled by on-chain governance.

### Extensive customizability

Based on these robust defaults, the feature set is highly customizable:

- **Permissioned EVM**- Implement customized access controls to either blacklist or whitelist individual addresses for calling and/or creating smart contracts on the network.
- **EVM Extensions** - Use custom EVM extensions to write custom business logic for your use case.
- **Single Token Representation v2 & ERC-20 Module** - The Single Token Representation v2 and our `x/erc20` module to aligns IBC and ERC-20 token representation to simplify and improve user experience.
- **EIP-1559 Fee Market Mechanism** - Customize fee structures and transaction surge management with the self-regulating fee market mechanism based on [EIP-1559 fee market](https://eips.ethereum.org/EIPS/eip-1559).
- **JSON-RPC Server** - There is full control over the exposed namespaces and [JSON-RPC server](https://AP CHAIN-docs.mintlify.app/docs/api-reference/ethereum-json-rpc). Configurable parameters include custom timeouts for EVM calls or HTTP requests, maximum block gas, open connections, and more.
- **EIP-712 Signing** - Integrate the [EIP-712 signature](https://eips.ethereum.org/EIPS/eip-712) implementation to allow AP CHAIN SDK messages to be signed with EVM wallets like MetaMask. This supports structured data signing for arbitrary messages.
- **Custom Improvement Proposals (Opcodes)** - Any AP CHAIN EVM user is provided the opportunity to customize bits of their EVM opcodes and add new ones. Read more on [custom operations here](https://AP CHAIN-docs.mintlify.app/docs/documentation/smart-contracts/custom-improvement-proposals#custom-improvement-proposals).

## Compatibility with Ethereum

Is AP CHAIN EVM "Ethereum equivalent"? Ethereum-equivalence describes any EVM solution that is identical in transaction execution to the Ethereum client. On the other hand, Ethereum-compatible means that the EVM implementation can run every transaction that is valid on Ethereum, while also handling divergent transactions that are not valid on Ethereum.

We describe AP CHAIN EVM as **forward-compatible** with Ethereum. It can run any valid smart contract from Ethereum and also implement new features that are not yet available on the standard Ethereum VM, thus moving the standard forward.

## Getting started

To run the example `evmd` chain, run the script using `./local_node.sh`
from the root folder of the repository.

### Migrations

We provide upgrade guides [here](./docs/migrations) for upgrading your chain from various AP CHAIN EVM versions.

### Testing

All test scripts are found in `Makefile` in the root of the repository.
Listed below are the commands for various tests:

#### Unit Testing

```bash
make test-unit
```

#### Coverage Test

This generates a code coverage file `filtered_coverage.txt` and prints out the
covered code percentage for the working files.

```bash
make test-unit-cover
```

#### Fuzz Testing

```bash
make test-fuzz
```

#### Solidity Tests

```bash
make test-solidity
```

#### Benchmark Tests

```bash
make benchmark
```


## Open-source License & Credits

AP CHAIN EVM is fully open-source under the Apache 2.0 license. It is a fork of [evmOS](https://github.com/evmos/OS). The Interchain Foundation funded [evmOS developers](https://github.com/evmos/OS) Tharsis to open-source the original evmOS codebase.  Tharsis and evmOS performed the foundational work for EVM compatibility and
interoperability in AP CHAIN.

## Developer Community and Support

The issue list of this repo is exclusively for bug reports and feature requests. We have active, helpful communities on Discord, Telegram, and Slack.

**| Need Help? | Support & Community: [Discord](https://discord.com/invite/interchain) - [Telegram](https://t.me/AP CHAINOG) - [Talk to an Expert](https://AP CHAIN.network/interest-form) - [Join the #AP CHAIN-tech Slack Channel](https://forms.gle/A8jawLgB8zuL1FN36) |**


## Maintainers
[AP CHAIN Labs](https://AP CHAINlabs.io/) maintains the core components of the stack: AP CHAIN SDK, CometBFT, IBC, AP CHAIN EVM, and various developer tools and frameworks. The detailed maintenance policy can be found [here](https://github.com/AP CHAIN/security/blob/main/POLICY.md). In addition to developing and maintaining the AP CHAIN Stack, AP CHAIN Labs provides advisory and engineering services for blockchain solutions. [Get in touch with AP CHAIN Labs](https://www.AP CHAINlabs.io/contact).

AP CHAIN Labs is a wholly-owned subsidiary of the [Interchain Foundation](https://interchain.io/), the Swiss nonprofit responsible for treasury management, funding public goods, and supporting governance for AP CHAIN.

The AP CHAIN Stack is supported by a robust community of open-source contributors.

## Contributing to AP CHAIN EVM

We welcome open source contributions and discussions! For more on contributing, read the [guide](./CONTRIBUTING.md).

### Key Contributors to AP CHAIN EVM

We would like to thank our key contributors at [B-Harvest](https://bharvest.io/) and 
[Mantra](https://www.mantrachain.io/) for contributing to and helping us drive the development of AP CHAIN EVM.

## Documentation and Resources

### Documentation
Visit the official documentation for AP CHAIN EVM: [evm.AP CHAIN.network](https://evm.AP CHAIN.network/)

### AP CHAIN Stack Libraries

- [AP CHAIN SDK](http://github.com/AP CHAIN/AP CHAIN-sdk) - A framework for building
  applications in Golang
- [The Inter-Blockchain Communication Protocol (IBC)](https://github.com/AP CHAIN/ibc-go/) - A blockchain interoperability protocol that allows blockchains to transfer any type of data encoded in bytes.
- [CometBFT](https://github.com/cometbft/cometbft) - High-performance, 10k+ TPS configurable BFT consensus engine.
