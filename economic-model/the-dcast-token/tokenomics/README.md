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
The implementation of the DCAST token is currently under careful scrutiny for its viability, as well as regulatory uncertainties that could classify it as a security token. It is crucial to note that any ERC20 contract currently being deployed under the name "DCAST" is not official and should be considered fraudulent.
{% endhint %}

### Maximum Supply

The total number of tokens is capped at _**100 million.**_



### **Allocations**

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

The total distribution of DCAST tokens will be as follows:

* _**Community**_: 79.2% (70.4% for commissions and 8.8% for one-time rewards)
* _**Investors (Private Seed)**_: 7%
* _**Strategic Reserve**_: 5% (3% for treasury and 2% for liquidity pools)
* _**Team**_ : 8.8%



### Circulating Supply Evolution

<figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

#### _Initialization of Supply_

Upon deployment of the `DCast.sol` contract, which marks the Token Generation Event (TGE), 5% of the total supply is immediately added to the project's strategic reserve.

#### _Vesting Plan for Investors_

* **Lock-up Period (**_cliff_**)**: Initial investors are subject to a one-year lock-up period during which no token allocations will be distributed.
* **Linear Distribution**: Following the cliff period, tokens allocated to investors will be distributed linearly over a three-year period, with monthly payouts. This ensures a gradual and controlled release of supply.
