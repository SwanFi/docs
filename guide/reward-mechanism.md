---
description: SwanFi Staking & Rewards – FAQs
---

# Reward Mechanism



#### **1. How does rebasing work in SwanFi?**

When you stake SWAN into SwanFi, you receive shares behind the scenes. Your balance is determined by:

**Formula:**\
`balanceOf(user) = (sharesOf(user) / getTotalShares()) * totalPooledSwan()`

This means your balance is a percentage of the total pooled SWAN.

* **When you stake SWAN:** `totalPooledSwan` increases.
* **When you withdraw SWAN:** `totalPooledSwan` decreases.
* **When the admin posts rewards:** The contract updates `totalPooledSwan`, increasing all users' balances automatically while their shares remain unchanged.

**2. How do I earn rewards on SwanFi?**

* When you stake SWAN into SwanFi, you receive **fSWAN**.
* The pooled SWAN is then staked into the **Parasail protocol** to earn **pSWAN**.
* Parasail has a rebasing mechanism where rewards are calculated whenever pSWAN is staked or withdrawn.
* Your rewards come from the **pSWAN staking wallet.**

#### **3. How are daily rewards calculated?**

Every day at **10 AM EST**, rewards are calculated using:

`todays_reward = (todays_pswan_balance - yesterdays_pswan_balance - incoming_pswan + outgoing_pswan) * 0.9`

**Important Notes:**

* Incoming pSWAN from transfers/stakes is excluded from rewards.
* If no one stakes/withdraws for 24 hours, no rewards are realized until a rebase is triggered.

**4. How can I withdraw my SWAN?**

1. **Request Withdrawal:** When you initiate a withdrawal, your **fSWAN is locked** in the withdraw wallet, starting a **3-day cooldown**.
2. **Processing:** The request is processed by our scanner, which then requests a withdrawal from Parasail.
3. **Completion:** Once SWAN is returned to SwanFi, the withdraw wallet **burns fSWAN** and returns SWAN to you.

**5.Does this affect other users?**\
No, since **both `totalPooledSwan` and `totalShares` decrease**, the balance of other users remains unchanged.
