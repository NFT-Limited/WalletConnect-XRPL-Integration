# WalletConnect-XRPL-Integration
## Introduction
Although the XRPL Xumm wallet has a complete platform around it to build and run applications it would be highly beneficial to the XRPL to have a generic protocol like WalletConnect implemented. WalletConnect is an open protocol to communicate securely between Wallets and Dapps (Web3 Apps). The protocol establishes a remote connection between two apps and/or devices using a Bridge server to relay payloads. These payloads are symmetrically encrypted through a shared key between the two peers.

Implementing the WalletConnect protocol would require building a XRPL implementation on the WalletConnect interface and a WalletConnect implementation on the XUMM wallet interface.

![walletconnect-xumm](https://user-images.githubusercontent.com/584523/195624778-8ae7a7e2-fa81-4aa3-b1f2-7ff549efea57.png)

## WalletConnect XRPL implementation
The WalletConnect protocol is an open protocol and its source code is publically available on Github. The current production version is 1.0 and is not suitable for adding an XRPL implementation. Version 2.0, which is currently in Beta release, does have the ability to add support for other blockchains. The following API specifications are available for implementation:
* Sign
* Chat
* Auth
* Push
* Core
From these API the minimal requirement for a working implementation would be the implementation of the Sign API. To allow for a more user friendly implementation the Push API would also have to be implemented.

## XUMM WalletConnect implementation
The second part for a WalletConnect implementation for the XRPL would consist of a wallet implementation. Currently the most widely used wallet for the XRPL is the XUMM wallet and its accompanying platform. Hence it would make sense to build the initial implementation arround XUMM. The following functionality would have to be implemented:
* Connect a wallet to a dapp by scanning a QRCode, for this the Xumm wallet would need to be able to recognize the WalletConnect QR Code for connecting a wallet
* Receiving and processing of WalletConnect event messages
* Handling of Signing and Submitting of transactions
* Managing push notifications

## Technical requirements
Both XUMM and WalletConnect projects are build using NodeJS, Typescript and React frameworks so similar coding knowledge is required for both. Initial investigation shows both platforms are open to receive and integrate a possible XRPL/XUMM integration for WalletConnect.

The WalletConnect required API version 2.0 is still in Beta but it is expected to be production release ready long before the XRPL implementation for WalletConnect would be finished.

## Deliverables
The following deliverables will be produced executing the project:
* Functional and tested WalletConnect implementation for the XRPL in a mergeable Github repository pull request for the WalletConnect GitHub
* Functional and tested XUMM implementation in a mergeable Github repository pull request for the XUMM Wallet
* Functional and tested WalletConnect Relay Server software
* Relay Server Installation Guide
* User Guide

