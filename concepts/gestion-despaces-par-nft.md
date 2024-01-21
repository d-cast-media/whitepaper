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

# Gestion d'espaces par NFT

### "_Tokeniser_" l'exposition à l'audience

d>sponsor révolutionne le financement des médias et des créateurs de contenus en permettant aux sponsors d'acquérir, de manière temporaire ou permanente, des encarts publicitaires.

La valeur de ces espaces de visibilité est définie par le marché, en se basant sur l'audience ciblée. L'utilisation des NFT (Tokens Non Fongibles) pour concrétiser ce potentiel d'exposition offre divers avantages significatifs :

* _**Suppression des intermédiaires**_** :** La technologie blockchain facilite des transactions directes entre le créateur et le sponsor, réduisant ainsi les coûts et les complications liés à la position dominante des intermédiaires.
* _**Preuve de propriété**_** :** Lorsqu'un sponsor acquiert un NFT associé à un encart publicitaire, il détient un certificat numérique irréfutable attestant de son droit exclusif sur cet espace.
* _**Implémentation simplifiée et interopérabilité**_** :** Le standard ERC721 des NFT facilite les développements, favorise la collaboration et l'intégration avec d'autres applications décentralisées.
* _**Flexibilité financière**_** :** Les transactions peuvent s'effectuer en différentes cryptomonnaies, et le sponsor a la possibilité de revendre ou de louer son NFT sur toute place de marché compatible.
* _**Authenticité et traçabilité**_** :** Chaque NFT est unique, et l'historique de son utilisation (origine, validité des publicités) est enregistré sur la blockchain, garantissant une transparence totale et l'authenticité de chaque encart.

L'intégration de la technologie NFT dans l'univers des médias ouvre une nouvelle ère de monétisation, offrant aux médias la possibilité de préserver leur indépendance tout en fournissant des informations de qualité et accessibles gratuitement.

### Interactions entre le Sponsor et le Créateur via d>sponsor

***

<figure><img src="../.gitbook/assets/dsponsor fr.png" alt=""><figcaption></figcaption></figure>

***

1. _**Création de l'offre de visibilité :**_ Le créateur spécifie les détails des espaces de visibilité. Chaque jeton (token) représente un espace unique. La collection NFT associée peut être déjà existante ou à créer. En cas de création, le créateur doit spécifier le nombre d'espaces et leur prix.
2. _**Définition de l'exposition :**_ Le créateur précise la durée de validité et décrit [l'exposition à son audience associée à l'offre](formes-de-sponsoring.md). Cela peut inclure, entre autres, une bannière web, un logo cliquable dans une newsletter, ou un pré-roll vidéo. Le créateur informe également les clauses de vente, les condtions d'utilisation associées au NFT que tout sponsor doit accepter en concluant l'achat d'un NFT.&#x20;
3. _**Acquisition d'un NFT :**_ Un sponsor intéressé par l'offre acquiert un NFT, devenant ainsi propriétaire de l'espace associé.
4. _**Proposition de publicité :**_ En tant que propriétaire du NFT, le sponsor a le droit de proposer une publicité pour cet espace. Par exemple, il peut soumettre un logo pour validation, en se conformant à l'exposition préalablement définie par le créateur.
5. _**Validation de la publicité proposée :**_ Le créateur approuve ou rejette la proposition du sponsor. Si elle est acceptée, l'espace est réservé pour cette publicité (un changement ultérieur restant possible). En cas de refus, le sponsor peut soumettre une nouvelle proposition, laissant l'espace vacant en attendant.

Toutes ces actions sont réalisées via des transactions associées à des [smart contracts](../technologie/smart-contracts/) déployés sur une blockchain.&#x20;

{% hint style="info" %}
<mark style="color:blue;">Remarques</mark>\


#### _Intégration des publicités validées_

Il incombe au créateur de correctement [intégrer et afficher les publicités approuvées](../technologie/modules-dintegration/) (par exemple, via une _iframe_ sur son site), tout en respectant ses engagements liés à l'exposition promise. Dans une version ultérieure, un mécanisme de pénalité décentralisé sera introduit, permettant aux sponsors estimant ne pas avoir bénéficié de l'exposition promise d'obtenir une compensation. Pour le calcul du [ROI](https://www.definitions-marketing.com/definition/roi/), voir la section "[Mesure de performance](lecosysteme-d-greater-than-sponsor.md#mesure-de-performance)" dédiée.&#x20;



#### _Modification de la publicité_&#x20;

Le sponsor peut à tout moment soumettre une nouvelle publicité, suivant le même procédé que les étapes 4. et 5.&#x20;



#### _Transfert de propriété_

Le sponsor peut vendre le NFT sur le marché secondaire (ex : [OpenSea](https://opensea.io/)), cédant ainsi la propriété de l'espace à un autre sponsor.\


#### _Option d'achat_&#x20;

Dans une version ultérieure, le sponsor pourra soumettre une offre d'achat conditionnée par l'approbation de sa publicité.
{% endhint %}

L'utilisation des NFT pour la gestion des espaces de visibilité transforme fondamentalement la manière dont le financement opère dans le secteur des médias et de la création. Cette approche procure une simplicité, une transparence et une flexibilité financière, offrant aux sponsors la possibilité d'optimiser leurs investissements tout en soutenant plus efficacement les créateurs.

