# Cardits — Carbon Credit Infrastructure on Blockchain

Cardits is a blockchain platform for issuing, verifying, and trading carbon credits with clear provenance. It reduces fraud and manual bottlenecks by making verification and credit movement transparent and auditable.

## Why this exists
Today’s carbon credit workflows can be slow and hard to verify. Credits may be double-counted, audits can be inconsistent, and market access is fragmented. That lack of visibility makes trust expensive and slows real climate action.

## What Cardits does
Cardits puts the full carbon credit lifecycle on-chain:

- Companies submit emissions or audit reports
- Auditors verify reports through DAO voting
- A regulator role mints verified credits
- Credits are listed and traded through a marketplace contract
- All state transitions remain publicly queryable for auditing

This removes silent edits and creates a single source of truth for report status, approvals, and transfers.

## How it’s built
High-level flow:

Company submissions → verification voting → credit minting → marketplace trading → public on-chain history

Everything important (roles, approvals, mint events, transfers) is recorded on-chain so anyone can validate what happened and when.

## Contract components
The core contracts are separated by responsibility:

- Role / ownership controls  
  Manages privileged actions (ex: regulator permissions)
- Verification (DAO voting)  
  Auditors approve or reject submitted reports
- Marketplace / auction  
  Trustless bidding and transfers for verified credits

Together, these contracts support permissioned issuance, decentralized validation, and transparent trading.

## Product surface (UI)
The frontend is designed to make status and actions easy to follow:

- Dashboard for tracking credits, emissions submissions, and compliance status
- Verification progress indicators and basic analytics
- Marketplace view to browse, bid, and purchase credits
- Wallet support via MetaMask and Ethers.js

## Tools and technologies
- Frontend: React, Material UI, React Router, Ethers.js
- Smart contracts: Solidity (0.8.x), Hardhat, Remix, Ethereum testnets (Sepolia/Goerli)
- Storage: On-chain reads today, with IPFS planned for audit documents

## Governance and roles
Cardits is designed around a clear separation of powers:

- Regulator: mints credits after verification (permissioned)
- Auditor DAO: votes on whether reports are valid
- Companies: submit reports but cannot approve their own submissions

All approvals and outcomes are visible on-chain.

## Current MVP
Implemented MVP scope includes:

- DAO-based emissions verification
- Role-based control for minting and privileged actions
- Auction/marketplace contract for credit trading
- React dashboard with wallet connection
- Report submission and verification status UI

## Roadmap ideas
Planned or potential extensions:

- ERC-1155 tokenized credits
- IPFS-backed storage for audit documents
- Fraud/anomaly detection to flag suspicious reports
- Fractional credit trading
- Multi-chain registry bridging

## Team
Built by:
- Ansh Kothari
- Ansh Tandon
- Aditya Kattil
- Partth Kulkarni

## Demo Video
https://github.com/user-attachments/assets/ed71dbec-3e5b-42d3-aae8-2e28216c0592


## Pitch
- [Deck](https://docs.google.com/presentation/d/1VTOBbh-rzx3xWxiVdeyhGtzoNUoMfpTAC8YXsrAszqE/edit?slide=id.g2e615814cae_0_57#slide=id.g2e615814cae_0_57)

## One-line summary
Cardits turns carbon credit issuance, verification, and trading into an auditable on-chain workflow where approvals are explicit, ownership is traceable, and market activity is transparent.
