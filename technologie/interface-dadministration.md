# Interface d'administration

{% hint style="warning" %}
L'architecture de l'interface d'administration est en cours de développement et les fonctionnalités présentées sont sujettes à des révisions ultérieures. Des visualisations concrètes de l'interface seront partagées pour offrir une meilleure compréhension de son fonctionnement.
{% endhint %}

### Fonctionnalités pour les médias et créateurs ([sponsorisés](../concepts/lecosysteme-d-greater-than-sponsor.md#acteurs-beneficiant-du-financement-via-d-greater-than-sponsor))

#### _**Création et gestion des offres de sponsoring**_

* Configuration des [collections NFT associées aux espaces de visibilité](../concepts/gestion-despaces-par-nft.md), incluant la définition des prix et des quantités.
* Fourniture d'informations pour l'[intégration](modules-dintegration/) des publicités sur diverses plateformes, tels que des modules _iframe_ pour les sites web.
* Espace de validation des publicités soumises par les sponsors, avec des indicateurs facilitant le contrôle de la qualité et la pertinence des données soumises.

#### _**Suivi des performances et gestion financière**_

* Outils d'analyse pour visualiser les ventes de tokens d'espaces de visibilité.
* Fonction pour retirer les [fonds accumulés à travers les ventes et les royalties](smart-contracts/#flux-financiers) de revente.

### Fonctionnalités pour les financeurs ([sponsors](../concepts/lecosysteme-d-greater-than-sponsor.md#acteurs-qui-financent-via-d-greater-than-sponsor))

* Catalogue d'espaces : parcours et achat d'espaces de visibilité tokenisés, classés par type de média et catégorie.
* Système de soumission permettant aux sponsors d'envoyer leurs annonces aux médias ou créateurs pour approbation.

### Fonctionnalités pour les apporteurs d'affaire ([parrains](../concepts/lecosysteme-d-greater-than-sponsor.md#parrains-apporteurs-daffaires))

* Création de liens d'affiliation personnalisés pour promouvoir la vente de tokens d'espaces de visibilité
* Tableau de bord pour le suivi des indicateurs de performance, incluant le trafic généré et les conversions réalisées via les liens d'affiliation.

### Expérience utilisateur optimisée

L'interface d'administration d>sponsor est conçue comme un portail intuitif, connectant les médias et les créateurs avec les sponsors dans un écosystème transparent et sécurisé, accessible à tous les niveaux d'utilisateurs de la blockchain.

#### _**Abstraction de compte**_

L'[Account Abstraction](https://cryptoast.fr/account-abstraction/) (AA) simplifie l'expérience utilisateur en permettant aux utilisateurs de s'inscrire et de se connecter via des méthodes familières telles que l'email ou les comptes de réseaux sociaux, sans avoir à interagir directement avec des clés privées. Les interactions avec la blockchain restent décentralisées et sécurisées, tout en offrant des options de récupération de compte pour répondre aux scénarios d'oubli de mot de passe ou de perte d'accès.

#### _**Paiement des frais de gas**_

L'interface prend en charge le paiement des frais de gas en arrière-plan dans certains cas (si l'utilisateur n'a pas de quoi les payer par exemple). Cela simplifie notamment le processus pour les non-initiés à la blockchain.
