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

# Récompenses

{% hint style="warning" %}
Le modèle de récompenses décrit ci-dessous est actuellement en phase de développement et pourrait être ajusté en fonction des exigences réglementaires avant son implémentation définitive.
{% endhint %}

La répartition des bénéfices générés par la trésorerie de d>sponsor constitue un pilier clé du protocole, ayant pour objectif de récompenser les détenteurs de [jetons verrouillés](./) (veDCAST/veDCASTLP) et de soutenir la croissance de l'écosystème.

### Rachat du DCAST

70% des bénéfices générés serviront à racheter du DCAST sur les marchés, afin d'être redistribué aux détenteurs des veTOKEN.

### **Répartition mensuelle des récompenses**

Au début de chaque mois, les DCAST rachetés sont alloués de la manière suivante :

* _**20% aux détenteurs de jetons veDCAST**_ : Cette proportion significative vise à maintenir un noyau robuste de détenteurs de jetons DCAST verrouillant leur jeton au sein du projet, créant ainsi un effet stabilisateur et une demande constante pour le jeton. Le calcul de la répartition se base sur le nombre de veDCAST, détenu à la première seconde du mois précédent, par rapport au total de veDCAST en circulation.
* _**50% aux fournisseurs de liquidité**_ _:_ Les fournisseurs de liquidité jouent un rôle essentiel dans la facilitation des échanges du jeton DCAST et sont récompensés généreusement pour compenser les pertes potentielles liées à l'_impermanent loss_, en particulier lors de fortes variations du cours du jeton. Le calcul de la répartition se base sur le nombre de veDCASTLP, détenu à la première seconde du mois précédent, par rapport au total de veDCASTLP en circulation.

Les 30% des bénéfices restants sont conservés par la trésorerie du protocole :

* _**15% pour les dépenses de fonctionnement**_ : Une partie des revenus est allouée à la réserve stratégique pour couvrir les frais opérationnels et autres dépenses nécessaires.
* _**15% pour la diversification**_ : Ces fonds sont dédiés à des investissements diversifiés, tels que des placements en DeFi ou des participations dans d'autres projets, pour renforcer la résilience financière du protocole.

### **Revenus éligibles aux récompenses**

La part de DCAST à racheter et la part trésorerie sont exclusivement calculés sur les [revenus perçus par la trésorerie](../../frais-percus-par-le-protocole.md) en MATIC, WETH, WBTC, USDC et USDT. 70% de chaque token est utilisé pour le rachat de DCAST. Les revenus provenant d'autres cryptomonnaies restent dans la trésorerie pour être utilisés ultérieurement.&#x20;

### **Exemple de calcul des récompenses**

Pour illustrer comment les détenteurs de jetons $DCAST pourraient bénéficier des revenus générés par la trésorerie d>sponsor, examinons un scénario basé sur les performances mensuelles suivantes :

* Revenus de la trésorerie :
  * 1 WBTC
  * 15 WETH
  * 50 000 USDC
  * 100 000 DAI
*   Part utilisée pour le achat de DCAST

    * 0,7 WBTC (70% de 1 WBTC)
    * 10,5 WETH (70% de 15 WETH)
    * 35 000 USDC (70% de 50 000 USDC)
    * 0 DAI (car le DAI n'est pas éligible aux récompenses)

    :arrow\_right: à un cours de 50 000$ le BTC, 3 000$ l'ETH, cela équivaudrait à 101 500$ de rachat de DCAST:arrow\_right: supposons un DCAST à 1$, cela équivaudrait à \~100 000 DCAST rachetés

Supposons qu'au début du mois en question un utilisateur détenait 30 000 veDCAST sur un total de 600 000 veDCAST, soit 5% du staking total de DCAST. Ce pourcentage le rend éligible pour 5% de la portion de 25% des revenus du mois dédiés aux détenteurs de veDCAST, soit 1.25% du total des récompenses. En conséquence, ce détenteur recevra :

* 0.0125 WBTC, équivalant à 1.25% de 1 WBTC
* 0.1875 WETH, équivalant à 1.25% de 15 WETH
* 625 USDC, équivalant à 1.25% de 50 000 USDC
* 0 DAI (car le DAI n'est pas éligible aux récompenses)

### **Impact sur le prix du jeton DCAST**

Le cours du jeton DCAST est soutenu par le verrouillage des jetons dans le protocole afin d'obtenir une part des revenus mensuels de la trésorerie. L'impact sur le prix sera d'autant plus grand que les frais captés par la trésorerie progresseront, incitant au verrouillage des jetons DCAST en circulation.
