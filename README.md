Web4 Demo on NEAR protocol
==========================

[Web4](https://web4.near.page) is a gateway to the smart contracts deployed to NEAR protocol.

This demo just shows the minimum viable application that lives on NEAR chain, and thus anyone hosting the gateway can serve all the Web4 projects!

See it live on testnet: https://hello-web4.testnet.page

When you deploy on mainnet, you should be able to use https://ACCOUNT_ID.near.page as your gateway.

## Build

See [near-sdk docs](https://near-sdk.io) for the prerequisites, and then build the contract:

```
$ cargo build --target wasm32-unknown-unknown --release
```

## Deploy

Using [near-cli-rs](https://near.cli.rs) you can deploy the contract to your account:

```
$ near-cli add contract-code network testnet account ACCOUNT_ID.testnet contract-file ./target/wasm32-unknown-unknown/release/web4_demo.wasm no-initialize sign-with-keychain
```