---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Fees collected

The economic model of d>sponsor is based on charging fees at two stages: at the initial creation of an NFT (minting fees) and at its resale on the secondary market (resale fees), **both currently set at 4%**.

These fees contribute to the d>sponsor treasury and are intended to ensure the sustainability of the [ecosystem ](../concepts/ecosystem.md)and the continued funding of the protocol.

### Fees Structure

Fees are collected at two different levels when an NFT representing a visibility space is issued by the protocol (via the [`DSponsorGroups.sol`](broken-reference), not by an external collection):

* _**Mint**_: Fees applied to the amount paid by the sponsor during the initial sale of the NFT.
* _**Resale**_: Fees on [royalties ](https://eips.ethereum.org/EIPS/eip-2981)from a secondary market transaction, if the marketplace supports this feature.

The d>sponsor treasury collects these fees regardless of the cryptocurrency used for the transactions.

#### _Example_

Let's consider the case of BigMedia offering an NFT linked to an ad space purchased by SponsorA for 100 USDC:

* BigMedia receives 96 USDC (96% of 100 USDC)
* The treasury receives 4 USDC (4% of 100 USDC)

If SponsorA resells this NFT to SponsorB for 200 USDC via a platform that takes 2.5% commission and 10% in royalties:

* SponsorA receives 175 USDC (87.5% of 200 USDC)
* BigMedia receives 19.20 USDC (96% of 10% of 200 USDC)
* The treasury receives 0.8 USDC (4% of 10% of 200 USDC)
* The marketplace gets 5 USDC (2.5% of 200 USDC)

### Purpose of Fees

The fees collected are used to cover various expenses, such as:

1. Compensating the technical, marketing, and administrative teams.
2. Conducting security audits.
3. Management of legal aspects to ensure project compliance.

[A portion of the revenues will be redistributed through a specific mechanism](the-dcast-token/vedcast-and-vedcastlp/rewards.md) linked to the [DCAST token](the-dcast-token/) to support the growth of the protocol and actively reward contributors to its expansion.
