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

# Modules d'intégration

La plateforme d>sponsor propose des modules d'intégration clé en main afin de faciliter l'affichage des publicités, tout en offrant une personnalisation avancée pour répondre aux besoins spécifiques des médias et créateurs.

### Intégrations (bientôt) disponibles via l'interface d'administration admin.dsponsor.com

* _**Widget HTML**_ : Un composant prêt à l'emploi, sans dépendance JavaScript ou CSS externe, spécialement conçu pour une intégration aisée dans toute page web ou email. Un simple copier-coller suffit pour insérer un [encart de logos cliquables](../../concepts/formes-de-sponsoring.md#encart-de-logos-cliquables) ou une [bannière dynamique](../../concepts/formes-de-sponsoring.md#banniere-dynamique).&#x20;
* _**URL d'image de bannière dynamique**_ : Cette URL stable conduit à une image qui se met à jour automatiquement, en faisant défiler au hasard une publicité parmi celles qui ont été validées au préalable. Il s'agit d'une manière efficace de diversifier l'affichage publicitaire sans que le créateur ait besoin de changer l'URL intégrée sur sa plateforme de contenus.

### Développement de nouveaux modules

#### _**Méthodes d'intégration et d'interaction avec d>sponsor**_

La création de modules personnalisés pour l'[affichage de données de sponsoring](../../concepts/formes-de-sponsoring.md#liberte-sur-la-forme-de-sponsoring) peut être abordée de diverses manières.&#x20;

{% content-ref url="requetes-on-chain.md" %}
[requetes-on-chain.md](requetes-on-chain.md)
{% endcontent-ref %}

{% content-ref url="api.md" %}
[api.md](api.md)
{% endcontent-ref %}

{% content-ref url="sdk.md" %}
[sdk.md](sdk.md)
{% endcontent-ref %}

#### _Spécifications de données_

Il est recommandé d'adopter le format de données suivant, bien que cela ne soit pas impératif :

```
{
  "property_payload_type": "string", // identifiant du format de sponsoring
  "property_payload_version": "string", // version en respectant le formalisme SemVer
  "content": "Object" // objet contenant les données du sponsoring
}
```

Un tel format JSON peut être stocké sur [IPFS](https://ipfs.tech/). Le CID correspondant est fourni au contrat [DSponsor.sol](../smart-contracts/#dsponsor.sol), permettant au module d'intégration de récupérer le contenu via IPFS.

* **Exemple pour l'**[encart de logos cliquables](../../concepts/formes-de-sponsoring.md#encart-de-logos-cliquables) :

```
{
  "property_payload_type": "ClickableLogo",
  "property_payload_version": "1.0.0",
  "content": {
    "logo": "https://exemple.com/logo.jpg",
    "link": "https://exemple.com/?utm_source=dsponsor"
  }
}
```

* &#x20;Exemple pour la [bannière dynamique](../../concepts/formes-de-sponsoring.md#banniere-dynamique) :

```
{
  "property_payload_type": "DynamicBanner",
  "property_payload_version": "1.0.0",
  "content": {
    "image": "https://exemple.com/banner.jpg",
    "text": "<p>Votre texte personnalisé ici avec <a href='https://exemple.com/?utm_source=dsponsor'>lien</a>.</p>"
  }
}

```

#### _Validité des données_&#x20;

Les modules d'intégration doivent inclure des mécanismes de vérification afin d'assurer la conformité des données fournies. Par exemple, s'assurer que les images sont de forme carrée ou que le contenu HTML ne comporte pas d'éléments potentiellement malveillants. Ces mesures sont essentielles pour garantir que les publicités répondent aux normes de qualité et de sécurité requises par les plateformes de diffusion, tout en préservant l'intégrité de l'expérience utilisateur.

