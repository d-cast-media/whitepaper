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

# Distribution des commissions

{% hint style="warning" %}
Le mécanisme de commission présenté est sujet à révision et n'a pas encore été finalisé.
{% endhint %}

Au début de chaque mois, les jetons DCAST sont répartis en fonction des revenus engendrés par la vente de NFT liés à des espaces de visibilité au cours du mois précédent. Ce processus rémunère tant l'acheteur (sponsor) que le vendeur (média/créateur), en plus de l'éventuel intermédiaire (apporteur d'affaires).

### Critères de calcul

La distribution de jetons DCAST est calculée en fonction des transactions de vente effectuées en USDC, MATIC, WETH et WBTC. Les paiements avec d'autres cryptomonnaies ne seront inclus que s'ils sont ultérieurement ajoutés à la liste blanche après une [décision de la gouvernance](../vedcast-and-vedcastlp/gouvernance.md). Cette approche sélective a pour objectif d'éviter toute manipulation artificielle de la répartition des récompenses et d'encourager l'apport en trésorerie d'actifs liquides et de valeur avérée.

Les contributions sont calculées en dollars américains, en utilisant le taux de change en vigueur lors de la distribution mensuelle des récompenses, qui intervient le premier jour de chaque mois.

Chaque dollar provenant de la vente d'un NFT est réparti équitablement : 50 centimes pour l'acheteur et 50 centimes pour le vendeur. Le modèle de parrainage propose une répartition tripartite des contributions : un tiers pour l'acheteur, un tiers pour le vendeur et un tiers pour l'apporteur d'affaires.&#x20;

La part totale des revenus de chaque acteur est calculée en fonction de l'activité globale du mois précédent, et les jetons DCAST sont ensuite distribués proportionnellement à cette part en fonction des revenus totaux du mois.

### Exemples de distribution

SponsorA acquiert un NFT de SmallCreator pour 10 WETH, générant 0.4 WETH pour la trésorerie ([4 % de frais](../../frais-percus-par-le-protocole.md)). équivalent à 1 000 $. La valeur totale des revenus captée par la trésorerie le mois précédent est de 20 000 $. La transaction représente donc 5% du total des revenus du mois précédent. [Sans aucun halving jusqu'à présent, l'allocation est de 1 million de jetons DCAST](../tokenomics/#distribution-des-jetons-pour-la-communaute-et-lequipe). SponsorA et SmallCreator se partagent alors 50 000 jetons $DCAST, recevant chacun 25 000.

Le même mois, SponsorB acquiert un NFT de BigMedia via un lien d'affiliation d'Agence3, pour 50 000 USDC, générant ainsi 2 000 USDC pour la trésorerie. Cette transaction constitue 10% des revenus avec le taux 1 USDC = 1 $. SponsorB, BigMedia et Agence3 se partagent alors 100 000 DCAST, recevant chacun 33 333.33 DCAST.

### Variation du montant des récompenses

Il est important de noter que le nombre de jetons DCAST attribués pour un montant de revenus identique peut varier d'un mois à l'autre, en fonction du volume total des transactions validées pendant la période concernée.
