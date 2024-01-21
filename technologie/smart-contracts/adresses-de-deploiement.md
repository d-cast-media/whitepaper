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

# Adresses de déploiement

{% hint style="warning" %}
Les smart contracts de d>sponsor sont actuellement en phase de développement et leur architecture comme leur implémentation subiront des changements avant leur lancement. Il n'est pas encore possible de les utiliser à ce stade.
{% endhint %}

Chaque contrat est déployé via un mécanisme de [proxy UUPS](https://ethereum-blockchain-developer.com/110-upgrade-smart-contracts/08-eip-1822-uups/).

### Réseaux de production ("Mainnets")

| Réseau      | Smart contract                                        | Addresse de déploiement |
| ----------- | ----------------------------------------------------- | ----------------------- |
| Polygon PoS | [DSponsorGroups.sol](./#dsponsorgroups.sol)           | 🔜                      |
| Polygon PoS | [DSponsor.sol](./#dsponsor.sol)                       | 🔜                      |
| Polygon PoS | [DSponsorDistributor.sol](./#dsponsordistributor.sol) | 🔜                      |
| Polygon PoS | [DSponsorHub.sol](./#dsponsorhub.sol)                 | 🔜                      |

### Réseaux de test

| Réseau | Smart contract                                        | Addresse de déploiement                    |
| ------ | ----------------------------------------------------- | ------------------------------------------ |
| Goerli | [DSponsorGroups.sol](./#dsponsorgroups.sol)           | 0xa30a36CF8AbFD57bF55de4989aaAa484a70fd3aD |
| Goerli | [DSponsor.sol](./#dsponsor.sol)                       | 🔜                                         |
| Goerli | [DSponsorDistributor.sol](./#dsponsordistributor.sol) | 0xc4aA47691D620A229788C2d9BAcB31A46A494569 |
| Goerli | [DSponsorHub.sol](./#dsponsorhub.sol)                 | 0x03765Cc238D4836639631AC737eCE9e4E1663B09 |
| Mumbai | [DSponsorGroups.sol](./#dsponsorgroups.sol)           | 0xa30a36CF8AbFD57bF55de4989aaAa484a70fd3aD |
| Mumbai | [DSponsor.sol](./#dsponsor.sol)                       | 🔜                                         |
| Mumbai | [DSponsorDistributor.sol](./#dsponsordistributor.sol) | 0xc4aA47691D620A229788C2d9BAcB31A46A494569 |
| Mumbai | [DSponsorHub.sol](./#dsponsorhub.sol)                 | 0x03765Cc238D4836639631AC737eCE9e4E1663B09 |
