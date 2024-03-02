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

* **Investors**: 7% (7M)
  * _<mark style="color:purple;">**Seed Round**</mark>_ : 7% (7M) - 1-year cliff, followed by 3-years vesting
* **Community**: 79.2% (79.2M)
  * The token issuance follows a **monthly distribution plan**: initially, 1 million tokens will be distributed each month for the first 44 months, allocated based on the activity of the previous month. At the end of this period, a **halving** of the monthly issuance will occur every 44 months, continuing until the total cap of 88 million issued tokens is reached.
  * _<mark style="color:purple;">**Active users**</mark>_: 70.4% (70.4M) (80% of the monthly distribution)
  * _<mark style="color:purple;">**Grants**</mark>_: 8.8% (8.8M) (10% of the monthly distribution)
* **Team**: 8.8% (8.8M) (10% of the monthly distribution)
  * identical distribution plan to the community
* **DAO**: 5% (5M)
  * _<mark style="color:purple;">**Treasury**</mark>_ : 3% (3M) - 5-years vesting&#x20;
  * _<mark style="color:purple;">**Liquidity Pools**</mark>_: 2% (2M) - TGE Issuance

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Token Allocation</p></figcaption></figure>

### Circulating Supply Evolution

<figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

#### _Initialization of Supply_

Upon deployment of the `DCast.sol` contract, which marks the Token Generation Event (TGE), 2% of the total supply is immediately allocated for liquidity pools, and 3% will go to the protocol's treasury, which will be unlocked linearly over 60 months.

#### _Vesting Plan for Investors_

* **Lock-up Period (**_cliff_**)**: Initial investors are subject to a one-year lock-up period during which no token allocations will be distributed.
* **Linear Distribution (**vesting**)**: Following the cliff period, tokens allocated to investors will be distributed linearly over a three-year period, with monthly payouts. This ensures a gradual and controlled release of supply.

#### _Token distribution for community and team_&#x20;

The DCAST tokens allocated to the community and team, representing 88% of the total supply, follow a vesting plan characterized by a monthly distribution with a halving mechanism every 44 months. This distribution strategy is designed to encourage long-term engagement within the community and among team members, rewarding initial commitment while encouraging continued development and expansion of the d>sponsor protocol.

The monthly distribution of DCAST tokens is directly tied to the activity and contribution to the protocol during the previous month. At the start of each month, the supply allocated to the community and the team is divided as follows:

* **Commissions for generated revenue**: The majority of the distribution, 80%, is paid out as commissions. These commissions are distributed in proportion to the revenue generated for the treasury during the previous month.

{% content-ref url="commission-distribution.md" %}
[commission-distribution.md](commission-distribution.md)
{% endcontent-ref %}

* **Team contribution** : Each month, 10% of the monthly distribution is reserved for d>sponsor team members who have actively contributed during the previous month.
* _**Grants**_ : Another 10% will be allocated as "grants", rewarding specific contributions that have a positive impact on the d>sponsor protocol. Initially, these rewards are decided by the team, then by [governance](../vedcast-and-vedcastlp/governance.md).

<details>

<summary>Calculation of total allocations</summary>

* **Commissions for generated revenue**: 80% of 88% of the total token supply = 70.4%&#x20;
* **Team contributions**: 10% of 88% of the total token supply = 8.8%
* **Grants** : 10% of 88% of the total token supply = 8.8%

</details>

This vesting plan is designed not only to increase buying pressure, but also to encourage active participation by token holders in the Protocol's continued revenue growth.\
By introducing a halving every 44 months, the reduced availability of new tokens to [capture a share of the protocol's revenue](../vedcast-and-vedcastlp/rewards.md) encourages strategic accumulation. However, as vesting progresses and new tokens are issued, existing holders see their relative share of future profits diluted. This dilution incentivizes holders to actively support and contribute to the ongoing expansion of the protocol. In practice, this means that token holders become partners in the growth of the protocol, attracted by the potential increase in revenue and valuation of the token they hold. This mechanism creates an ecosystem in which the alignment of interests between token holders and the growth of the protocol is essential to its long-term success.

### **Price and valuation of DCAST token**

The price of DCAST is determined by market forces on decentralized exchange platforms such as Balancer or Uniswap, where the supply and demand of participants determine its real-time value.
