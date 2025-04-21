# Address Binding Protocol

## Introduction

This document describes a protocol for linking on-chain CKB addresses with an off-chain identity within the DAO governance system. The protocol aims to ensure the system remains transparently verifiable and user-friendly to encourage maximum participation.

> This document is currently in the early concept phase and will change significantly.

## Background

One of the most important lessons learned from the first Community Fund DAO is that user-friendly interfaces are critical for adoption. Community members will not participate in a platform that is difficult to use. The first iteration used a flexible process with simple implementation, but user-friendliness suffered as a result.

Balancing user-friendliness with developer-friendliness is a challenge, but this expermient has given us unignorable results. This protocol attempts to balance these two goals, but prioritizes user-friendliness over simplistic implementation.

## Protocol Overview

The CKB native token is the basis for weighting votes in the DAO, and the addresses which hold the CKB must be bound to the accounts of the DAO. This creates a challenge in that we must bind on-chain addresses to off-chain identities using disconnected wallets which could change addresses or balances at any time.

Delegation of responsibility from an address to an off-chain signer provides a higher amount of flexibility. Once we have proved ownership of an address, the delegated signer can sign transactions on behalf of the address. This is a secure and flexible solution, but the challenge is that we still need to prove ownership of the address.

The process to prove ownership of an address is not unlike the process of the current DAO. The reasons that the current implementation failed to get traction with the community are:

1. The binding process is highly unfriendly to users. Not even technical users are able to intuitively understand the process without a detailed guide.
1. The binding process is repetitive and laborious. Users must go through the ardjuous process multiple times for each address they wish to bind.
1. Using an new address requires the user to go through the binding process again.
1. Only one wallet is supported even though there are multiple wallets that can be used within the ecosystem.
1. The 30-day lockup requirement of the Nervos DAO is a barrier that some users are not willing to accept.

The protocol described in this document aims to solve points 1, 2, and 3. While still relevant, point 4 and 5 are challenges that are not specifically addressed by this protocol.

The general flow is as follows:

- The process begins with a user who has created a DAO account and wants to bind an address to their account.
- The user clicks on the DAO Binding page from the navigation. They are prompted to create a key pair using WebAuthn. The DAO associates this public key with their account. 
- From the binding page, an API key is generated which is unique to their account. Instructions on the page tell the user to copy and paste the API key into the appropariate field of a supported wallet.
- They launch their wallet and click the DAO Binding button. It prompts for the API key which the user provides.
- The wallet then queries the DAO API and brings up their account information so they can be assured that the API key is valid and connected to the correct account.
- The wallet then dispalys a list of all of their addresses with balances, and asks the user to select the address they wish to bind. All addresses are selected by default.
- The wallet then generates a batch processing request for all of the selected addresses, generates the appropriate signatures, and binds the addresses to the public keys that are associated with their account.
- The wallet gives the option to retain the API for keeping addresses up to date using the API.
- Wallets which only support a single address will not have to update regularly. However, wallets which use multiple addresses for privacy, such as Neuron, should automatically check and update the bound addresses every time the wallet is launched.


