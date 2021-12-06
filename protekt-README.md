![Banner](/img/banner.jpg)

# Paymagic Documentation
[Protekt Protocol](https://protektprotocol.com/) makes DeFi secure and safe for mainstream users and institutionals. The protocol researches, rates, and wraps the best projects in DeFi, so users can confidently deposit into this new financial infrastructure. The goal is to support and catalyze the growth of the DeFi ecosystem by protecting users from getting rekt.

**Repos**
* [Smart Contracts](https://github.com/ProtektProtocol/protekt-protocol-contracts)
* [Frontend](https://github.com/ProtektProtocol/protekt-frontend)
* [Docs](https://github.com/ProtektProtocol/protekt-protocol-docs)

## DeFi Risk
Building on the work of awesome projects like [DeFi Score](https://defiscore.io/), [Nexus Mutual](https://nexusmutual.io/), [Aave's Safety Modules](https://docs.aave.com/aavenomics/safety-module), and others, we believe that large technical vulnerabilities are the **biggest risk to a thriving DeFi community** over the next few years. Smart contracts that contain large amounts of value face the following risks:
1. Smart Contract Risk - Technical bugs that can expose funds to hackers
2. Centralization Risk - Centralized admin keys are stolen or used nefariously or oracles are manipulated to allow an exploit
3. Financial Risk - Collateral falls below outstanding obligations, likely due to price movement, or low liquidity leads to locked funds

Especially as new money legos are created, snapped together, and remixed weekly, the risks multiply and become a bottleneck to more capital flowing into the space. New entrants need signaling and assurance of the projects they can trust and commit capital as well as recapitalization if a [Shortfall Event](https://docs.aave.com/aavenomics/terminology#shortfall-event-se) occurs.

To fulfill this need, Protekt introduces a new insurance protocol with several innovative features:
* 💸 Insurees can mint wrapped tokens with built in coverage (never "buy cover")
* 🛡 Stakers (shield miners) deposit capital to assume liability and earn rewards
* 🤝 Distributors earn rewards for onboarding new users
* 🔀 Configurable claims process via automated rules or a DAO
* 🏦 Payouts trigger a liquidation waterfall to spread risk through tranches

The protocol  was inspired and uses money legos from yearn, Aave, Compound, Balancer, Maker, rDAi, Nexus, and others. The very best in DeFi.

## How it works
Protekt Protocol allows any smart contract to be backed by a **Protekt Contract**, which creates a market for the risk of lost assets held by the smart contract. Each Protekt contract is a wrapper on a yield bearing token, like Compound cTokens and Aave aTokens, and provide built in coverage against different risks of lost capital. Each Protekt contract is a token itself, called a **pToken**.

On the other side of the market, shield miners stake tokens to assume the liability of one or more pTokens, depending on their risk tolerance. They earn rewards for their service but can be liquidated if an exploit occurs and a successful claim is approvedd.

![Protocol Comparison Diagram](/img/pcDAI-paUSDC.png)

For example, users can deposit Dai that gets forwarded into the Compound cDAI pool and get pTokens (pcDAI) in return. pcDAI represents your underlying cDAI 1:1 plus 80% of the COMP farming rewards, while the other 20% goes to the shield miners as rewards. This fee is the user's ongoing "premium" for purchasing cover. pTokens can be minted at any time and redeemed for your cTokens + adjusted COMP rewards at any time.

**In short, by holding a pToken, you pay 20% of your yield farming returns to be insured against hacks and smart contract bugs in the underlying capital pool.**

![pToken Image](/img/pTokenDiagram.png)

## The PTK Token
The [PTK token](/ptk-token.md) is the governance and rewards token of the Protekt Protocol. It will be used to stake for assuming protocol liability, make governance decisions, receive rewards from protocol fees, provided as protocol incentives, and used to fund grants and audit reports for DeFi protocols that are covered by Protekt.

### Protocol Incentives (Yield Farming)
PTK tokens can be earned by contributing capital (liquidity mining) and work, like completing tasks, writing documentation, writing code, translations, etc. 

New rounds of PTK will be claimable by those completing tasks to support the protocol. Read more about protocol [contributions and rewards here](/contributions-and-rewards.md).

### Governance
Governance will start and end with the Protekt community. The community will not only be PTK holders but also the hackers, devs, auditors, analysts, and actuaries that contribute their blood, sweat, and tears to DeFi. They will be the ones to propose coverage of new DeFi pools, adjust and critique settings, and keep DeFi safe at night. The protocol will maintain some level of centralization at the beginning so it can iterate quickly but will pursue a pathway of [progressive decentralization](https://a16z.com/2020/01/09/progressive-decentralization-crypto-product-management/) over time.

## References
* [Twitter](https://twitter.com/protektprotocol) for announcements
* [Telegram](https://t.me/protektdefi) for discussions
* [Snapshot (Coming Soon)](/) for governance
* [Github](https://github.com/corbinpage/protekt-protocol-docs) for code & docs
* [Original pitch from EthOnline](https://www.youtube.com/watch?v=7Az70o8kZy8&feature=youtu.be)