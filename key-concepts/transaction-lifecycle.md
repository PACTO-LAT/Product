# Transaction Lifecycle

Every Pacto transaction follows a **role-based, escrow-secured flow** that ensures no funds are released until all conditions are met.

All interactions happen via a smart escrow contract, powered by **Trustless Work**, and executed directly by the involved parties — not by Pacto.

***

### 1. Discovery

Either the buyer or the seller can initiate a trade. One party discovers the other through Pacto’s peer directory or listing system.

They review:

* Asset being sold (e.g. USDC)
* Fiat method and currency
* Location (if in person)
* Price and spread (e.g. $100 USDC for $102 cash)
* Terms (bank, cash, proof requirements)

***

### 2. Agreement

Both parties agree on the terms of the trade and trigger escrow creation via the Pacto dApp or mobile interface.

***

### 3. Escrow Creation

A **Trustless Work smart escrow** is created with roles:

* **Seller**: Sells the on-chain asset (e.g. USDC), funds the escrow, and will later confirm the fiat payment
* **Buyer**: Sends the off-chain fiat payment, provides evidence, and will receive USDC
* **Dispute Resolver** _(optional)_: Can intervene in case of disputes

The seller deposits the agreed amount (e.g. 100 USDC) into the escrow and **marks the milestone as done** — signaling readiness for the buyer to proceed.

***

### 4. Fiat Transfer

The buyer initiates the off-chain fiat transfer (e.g. in-person cash, mobile money, or bank deposit).

They **upload evidence** (e.g. a screenshot or reference number) and **approve the milestone** within the app.

***

#### 5. Confirmation & Release

The seller receives the fiat and **confirms** it inside the escrow contract by signing the release.

Once confirmed:

* The escrow logic is triggered
* USDC is released from the contract
* The buyer receives funds at their address

***

#### 🚨 6. Dispute Path (If Needed)

If either party disputes the milestone:

* The escrow enters **dispute status**
* The predefined **Dispute Resolver** (a Pacto agent or third party) is empowered to review the situation
* This agent can sign the final approval or cancel the release
* All decisions are **on-chain, transparent, and rule-based**

***

#### ✨ Outcome

* Neither party has to trust the other upfront
* Escrow logic guarantees safety and fairness
* Pacto and Trustless Work remain **non-custodial facilitators**
* Anyone can safely onboard/offboard via stablecoins
