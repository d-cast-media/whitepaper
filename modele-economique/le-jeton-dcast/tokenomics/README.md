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

# Tokenomics

{% hint style="warning" %}
L'implémentation du jeton DCAST est actuellement soumise à un examen minutieux concernant sa viabilité, ainsi qu'à des incertitudes réglementaires qui pourraient le classer comme un _security token_. Il est crucial de noter que tout contrat ERC20 actuellement déployé sous le nom de “DCAST” n'est pas officiel et doit être considéré comme frauduleux.
{% endhint %}

### **Offre maximale**

Le nombre total de jetons est fixé à _**100 millions**_.

### **Allocations**

<figure><img src="../../../.gitbook/assets/allocations.png" alt=""><figcaption></figcaption></figure>

La distribution totale des tokens DCAST est prévue comme suit:

* _**Communauté**_ : 79.2% (70.4% pour les commissions et 8.8% pour les récompenses ponctuelles)
* _**Investisseurs**_** (Private seed)** : 7%
* _**Réserve stratégique**_ : 5% (3% pour la trésorerie et 2% pour les pools de liquidité)
* _**Équipe**_ : 8.8%



### **Évolution de l'offre en circulation**

<figure><img src="../../../.gitbook/assets/evolution de l&#x27;offre en circulation (1).png" alt=""><figcaption></figcaption></figure>

#### _**Initialisation de l'offre**_

Dès le déploiement du contrat `DCast.sol`, marquant l'événement de génération de jeton (TGE), 5% de l'offre totale est immédiatement allouée à la réserve stratégique du projet.

#### _**Plan de vesting pour les investisseurs**_

* **Période de blocage (**_cliff_**)** : Les investisseurs initiaux seront soumis à une période de blocage d'un an, au cours de laquelle aucune allocation de jetons ne sera distribuée.
* **Distribution linéaire** : À l'issue de cette période de _cliff_, les jetons destinés aux investisseurs seront distribués de manière linéaire sur une période de trois ans, avec des versements mensuels. Cela garantit un déblocage progressif et maîtrisé de l'offre.

#### _**Distribution des jetons pour la communauté et l'équipe**_&#x20;

Les jetons DCAST alloués à la communauté et à l'équipe, représentant 88% de l'offre totale, suivent un plan de vesting caractérisé par une distribution mensuelle assortie d'un mécanisme de halving tous les 44 mois. Cette stratégie de distribution vise à stimuler un engagement durable au sein de la communauté et parmi les membres de l'équipe, honorant l'implication initiale tout en encourageant une évolution constante et une expansion continue du protocole d>sponsor.

1. <mark style="background-color:yellow;">Détails de l'émission mensuelle et du halving</mark>

En prenant en compte que la création du jeton a lieu au mois N :

* **À chaque début des mois N+1 à N+44**: 1% de l'offre totale, soit 1 million de jetons DCAST, est distribué. Au mois N+44, 44% de l'offre totale aura été émise pour la communauté et l'équipe.
* **À chaque début des mois N+45 à N+88**: Après le premier halving, la distribution mensuelle est réduite de moitié à 0,5%, soit 500,000 DCAST par mois. À la fin de cette période, 22% supplémentaires de l'offre totale auront été distribués, portant le total à 66% émis pour la communauté et l'équipe.
* **À chaque début des mois N+89 à N+132**: Un second halving réduit la distribution mensuelle à 0.25%, soit 250,000 DCAST. À la fin de cette période, 11% supplémentaires de l'offre totale auront été distribués, amenant le total à 77% émis pour la communauté et l'équipe.
* **Et ainsi de suite**: Le processus de halving se poursuit, réduisant la distribution mensuelle et prolongeant la période de vesting, conformément à une série géométrique qui converge vers 88% de l'offre totale distribuée.

2. <mark style="background-color:yellow;">Une distribution mensuelle basée sur l'activité</mark>

Pour les jetons alloués à la communauté et à l'équipe de d>sponsor, la distribution mensuelle des jetons DCAST est directement liée à l'activité et à la contribution au protocole durant le mois précédent. Le total de 88% de l'offre allouée à la communauté et à l'équipe est subdivisé comme suit à chaque début de mois :

* _**Commissions pour revenus apportés**_ : La majeure partie de la distribution, soit 80%, est versée sous forme de commissions. Ces commissions sont distribuées proportionnellement aux revenus générés pour la trésorerie au cours du mois précédent.

{% content-ref url="distribution-des-commissions.md" %}
[distribution-des-commissions.md](distribution-des-commissions.md)
{% endcontent-ref %}

* _**Contributions de l'équipe**_ : Chaque mois, 10% de la distribution mensuelle est réservée aux membres de l'équipe de d>sponsor qui ont activement contribué au cours du mois précédent.
* _**Grants**_ : Un autre 10% est attribué sous forme de "grants", récompensant des contributions spécifiques qui ont un impact positif sur le protocole d>sponsor. Initialement, ces récompenses sont décidées par l'équipe, puis par [gouvernance](../vedcast-and-vedcastlp/gouvernance.md).

<details>

<summary>Calcul des allocations totales</summary>

* **Commissions pour revenus apportés** : 80% de 88% de l'offre totale de jetons = 70.4%&#x20;
* **Contributions de l'équipe** : 10% de 88% l'offre totale de jetons = 8.8%
* **Grants** : 10% de 88% l'offre totale de jetons = 8.8%

</details>

Ce plan de vesting vise non seulement à renforcer la pression acheteuse, mais également à encourager un engagement actif des détenteurs de jetons dans la croissance continue des revenus du protocole.\
En introduisant un halving tous les 44 mois, la disponibilité réduite des nouveaux jetons pour [capturer une part des revenus du protocole](../vedcast-and-vedcastlp/recompenses.md) incite à une accumulation stratégique. Toutefois, à mesure que le vesting progresse et que de nouveaux jetons sont émis, les propriétaires existants voient leur part relative dans les bénéfices futurs se diluer. Cette dilution incite les détenteurs à soutenir activement et à contribuer à l'expansion constante du protocole. En pratique, cela signifie que les détenteurs de jetons deviennent des partenaires dans la croissance du protocole, attirés par l'augmentation potentielle des revenus et la valorisation du jeton qu'ils détiennent. Ce mécanisme crée un écosystème où l'alignement des intérêts entre les détenteurs de jetons et la croissance du protocole est essentiel pour le succès à long terme.

### Prix et valorisation du jeton DCAST

Le prix du DCAST est déterminé par les forces du marché sur des plateformes d'échanges décentralisées telles que Balancer ou Uniswap, où l'offre et la demande des participants déterminent sa valeur en temps réel.
