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

# Smart contracts

d>sponsor se distingue en tant que solution de monétisation décentralisée, orchestrant les interactions entre les créateurs de contenu et les sponsors exclusivement via des smart contracts sur une blockchain, garantissant ainsi l'absence de contrôle par des intermédiaires. Ce système, _permissionless_ et insensible à la censure de tiers, repose sur une architecture où même les développeurs de d>sponsor ne détiennent aucun pouvoir discrétionnaire.

### Code des contrats

{% hint style="danger" %}
Il est important de souligner que le développement en est à ses balbutiements, et le code disponible représente une ébauche préliminaire. Il n'est pas destiné à être une référence définitive et continuera à subir des modifications substantielles.
{% endhint %}

{% @github-files/github-code-block url="https://github.com/d-cast-media/dsponsor" %}

### Modélisation de la propriété des espaces de visibilité : collection NFT (ERC721)

Les droits publicitaires sur les espaces de visibilité sont représentés par des NFT, basés sur le standard [ERC721](https://ethereum.org/fr/developers/docs/standards/tokens/erc-721/).  Ces NFT peuvent être émis soit par le smart contract `DSponsorGroups.sol`, géré par le protocole d>sponsor, soit par une collection déjà existante.

#### `DSponsorGroups.sol`

Ce contrat gère la collection de NFT créée par d>sponsor, en utilisant un système d’indexation permettant de diviser la collection en [![2^128](data:image/gif;base64,R0lGODlhGwAVAOYAAAAAAAICAgcHBwoKCg0NDQ4ODhsbGx8fHyEhISIiIiQkJCcnJysrKywsLDQ0NDw8PD09PUBAQEZGRkdHR0hISEtLS01NTU5OTk9PT1BQUFdXV1hYWFlZWVpaWltbW1xcXF5eXmFhYWRkZGVlZWpqamxsbG5ubnBwcHR0dHp6ent7e39/f4CAgISEhIWFhYyMjJGRkZSUlJaWlpmZmZqampubm56enp+fn6CgoKGhoaampqioqKurq7CwsLa2tre3t7u7u729vb6+vsDAwMPDw8TExNLS0tPT09TU1NXV1djY2NnZ2d7e3uDg4Ojo6O3t7e/v7/Dw8PLy8vPz8/X19ff39/n5+fr6+vv7+/z8/P39/f7+/v///wAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAACwAAAAAGwAVAAAH0YBcgoOEhYaHiDcYF4JbKyUTLoI0Gh4piINKQRSCRQ5cUwJITwlbXBBJmIJDnFxWRoIMRFIFTVwSUKpcrIVOCFVcNgMVPLq7rYJaGkBcUBY5EwZMuryCWSI/gjMxgiYvgk0bDwsVS4PVViBCXFUwNSqCIzWCCy2uFgpYXD0cBy5XLAgoUHAABRYSIzqcyMJFS4QdgnwAQGLMmI4AuSqquvBBoyoaDaJ4RARDgsiRhbScCHGFy5N1KLlQyaDhCBIkMk7E5IIDgM+fOncKHUq06NBAADs=)](https://www.wolframalpha.com/input/?i=2%5E128) groupes. Chaque groupe correspond à une offre publicitaire distincte avec un nombre fixe de NFT (pouvant aller jusqu'à [![2^128](data:image/gif;base64,R0lGODlhGwAVAOYAAAAAAAICAgcHBwoKCg0NDQ4ODhsbGx8fHyEhISIiIiQkJCcnJysrKywsLDQ0NDw8PD09PUBAQEZGRkdHR0hISEtLS01NTU5OTk9PT1BQUFdXV1hYWFlZWVpaWltbW1xcXF5eXmFhYWRkZGVlZWpqamxsbG5ubnBwcHR0dHp6ent7e39/f4CAgISEhIWFhYyMjJGRkZSUlJaWlpmZmZqampubm56enp+fn6CgoKGhoaampqioqKurq7CwsLa2tre3t7u7u729vb6+vsDAwMPDw8TExNLS0tPT09TU1NXV1djY2NnZ2d7e3uDg4Ojo6O3t7e/v7/Dw8PLy8vPz8/X19ff39/n5+fr6+vv7+/z8/P39/f7+/v///wAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAACwAAAAAGwAVAAAH0YBcgoOEhYaHiDcYF4JbKyUTLoI0Gh4piINKQRSCRQ5cUwJITwlbXBBJmIJDnFxWRoIMRFIFTVwSUKpcrIVOCFVcNgMVPLq7rYJaGkBcUBY5EwZMuryCWSI/gjMxgiYvgk0bDwsVS4PVViBCXFUwNSqCIzWCCy2uFgpYXD0cBy5XLAgoUHAABRYSIzqcyMJFS4QdgnwAQGLMmI4AuSqquvBBoyoaDaJ4RARDgsiRhbScCHGFy5N1KLlQyaDhCBIkMk7E5IIDgM+fOncKHUq06NBAADs=) ](https://www.wolframalpha.com/input/?i=2%5E128)tokens par groupe). Les NFT d'espaces de visbilité peuvent être vendus sans restriction de prix ou d'acquéreur (en coin natif ou [ERC20](https://ethereum.org/fr/developers/docs/standards/tokens/erc-20/), conformément aux termes fixés par le créateur).

Chaque émission de NFT est assortie d'une commission de 4% reversée à la [trésorerie du projet d>sponsor](../../modele-economique/tresoreries.md). En cas de définition de [royalties](https://eips.ethereum.org/EIPS/eip-2981) par le créateur (par exemple, 10% sur la revente d'un NFT), la trésorerie de d>sponsor perçoit également 4% de ces royalties. Des explications détaillées sur la répartition des fonds sont fournies dans la section "[Flux financiers](./#flux-financiers)" ci-dessous.

{% hint style="info" %}
Actuellement, une étude est en cours intégrer le contrat[`PublicLock.sol` d'Unlock Protocol](https://docs.unlock-protocol.com/core-protocol/public-lock/), dans le but de tirer parti de fonctionnalités avancées pour la création et la gestion de collections NFT.
{% endhint %}

### Contrat de gestion des données de sponsoring

#### `DSponsor.sol`

Le contrat `DSponsor.sol` constitue le socle du système de droits publicitaires au sein du protocole d>sponsor, définissant avec précision les conditions et les spécifications des espaces publicitaires disponibles, tels que les emplacements réservés aux logos.

Chaque instance de `DSponsor.sol` est indissociablement liée à un contrat NFT spécifique, tel que `DSponsorGroups.sol`, ou tout autre contrat suivant la norme [ERC721](https://ethereum.org/fr/developers/docs/standards/tokens/erc-721/). Le contrat `DSponsor.sol` supervise le processus de soumission de contenu publicitaire par un sponsor, qui, en tant que détenteur d'un NFT, détient le droit exclusif lié à celui-ci de proposer des publicités.

Parallèlement, le contrat `DSponsor.sol` octroie aux créateurs le pouvoir d'examiner et de statuer sur la validité de ces propositions. La validation ou le rejet des publicités est consigné au sein de la blockchain sous forme d'événements, offrant ainsi un mécanisme transparent et vérifiable pour les intégrations tierces, qui s'appuient sur ces données pour orchestrer l'affichage des publicités approuvées.

Cette structuration assure une chaîne de responsabilités transparente, depuis la proposition de l'espace publicitaire jusqu'à son approbation finale, garantissant l'intégrité et la conformité des opérations.

### Flux financiers

#### `DSponsorDistributor.sol`

Les revenus générés par la création et la revente de NFT via `DSponsorGroups.sol` sont reversées à travers un système de répartition sécurisé. Cette approche vise à mettre en œuvre le principe du "[_pull payment_](https://fravoll.github.io/solidity-patterns/pull\_over\_push.html)", une méthode de transfert de valeur recommandée en Solidity, tout en centralisant la réception des royalties. Le contrat `DSponsorDistributor.sol` instaure ces mécanismes, où 96% des fonds sont destinés au créateur, tandis que 4%  alimentent la [trésorerie du projet d>sponsor](../../modele-economique/tresoreries.md).

#### `DSponsorHub.sol`

Les pourcentages de frais alloués à la trésorerie du projet sont sujets à être modifiés par la gouvernance (via le [jeton $DCAST](../../modele-economique/le-jeton-dcast/)). Le contrat `DSponsorHub.sol`est chargé de gérer ces ajustements, assurant ainsi une transparence et une flexibilité accrues dans le modèle financier du protocole.

### Schéma UML

<figure><img src="../../.gitbook/assets/uml solidity contracts (2).svg" alt=""><figcaption></figcaption></figure>
