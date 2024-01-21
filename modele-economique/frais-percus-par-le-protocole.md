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

# Frais perçus par le protocole

Le modèle économique de d>sponsor repose sur la perception de frais à deux niveaux : lors de la création initiale d'un NFT (frais de "Mint") et lors de sa revente sur le marché secondaire (frais de "Revente"), **fixés actuellement à 4%**.&#x20;

Ces frais contribuent à la trésorerie de d>sponsor et visent à assurer la soutenabilité de [l'écosystème](../concepts/lecosysteme-d-greater-than-sponsor.md) et le financement continu du protocole.

### Structure des frais

Des frais sont perçus à deux niveaux distincts lorsqu'un NFT représentant un espace de visibilité est émis par le protocole (via le contrat [`DSponsorGroups.sol`](../technologie/smart-contracts/#contrat-de-gestion-des-donnees-de-sponsoring), et non par une collection externe) :

* _**Mint**_ : Frais appliqués sur le montant payé par le sponsor lors de la première vente du NFT.
* _**Revente**_ : Frais sur les _redevances (_[_royalties_](https://eips.ethereum.org/EIPS/eip-2981)_)_ issues d'une transaction opérée sur le marché secondaire, si la marketplace supporte cette fonctionnalité.

La trésorerie d>sponsor capte ces frais indépendamment de la cryptomonnaie utilisée pour les transactions.&#x20;

#### _Exemple_

Prenons le cas de BigMedia qui propose un NFT lié à un espace publicitaire, acheté pour 100 USDC par SponsorA:

* BigMedia reçoit 96 USDC (96% de 100 USDC)
* La trésorerie reçoit 4 USDC (4 % de 100 USDC)

SponsorA revend ce NFT à SponsorB pour 200 USDC via une plateforme qui prend une commission de 2.5% et des royalties de 10% :

* SponsorA reçoit 175 USDC (87.5% de 200 USDC)
* BigMedia reçoit 19,20 USDC (96 % de 10% de 200 USDC)
* La trésorerie reçoit 0.8 USDC (4 % de 10% de 200 USDC)
* La marketplace reçoit 5 USDC (2.5% de 200 USDC)

### Finalité des frais

Les frais collectés sont destinés à couvrir diverses dépenses, telles que :

1. Rémunération des équipes techniques, marketing et administratives.
2. Réalisation [d'audits de sécurité](../technologie/smart-contracts/audits.md).
3. Gestion des aspects légaux assurant la conformité du projet.

[Une part des revenus sera redistribuée avec un mécanisme spécifique](le-jeton-dcast/vedcast-and-vedcastlp/recompenses.md) lié au [token DCAST](le-jeton-dcast/), ceci afin de soutenir la croissance du protocole et récompenser activement les contributeurs à son expansion.
