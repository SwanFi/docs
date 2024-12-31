# SwanFi OP Reward Pool

### Overview

The SwanFi OP Reward Pool is a dedicated program to reward Swan token holders with OP tokens. This initiative aligns with Swan Chain’s mission to incentivize participation and expand the DePIN (Decentralized Physical Infrastructure Network) ecosystem. By staking Swan tokens, users earn OP rewards based on dynamic factors such as Total Value Locked (TVL), baseline targets, and performance boosts.

***

### Key Features

#### 1. Staking for OP Rewards

* Users stake Swan tokens on SwanFi and receive **OP tokens** as rewards.
* Rewards are distributed daily and dynamically adjusted based on staking metrics.

#### 2. Dynamic Reward Adjustments

* The reward pool is influenced by:
  * Baseline TVL growth.
  * Boost multipliers for high performance.
  * Penalty multipliers for underperformance.

#### 3. Daily Reward Cap

* Maximum daily distribution of OP tokens is capped at **625 OP tokens** to ensure sustainability.

***

### How It Works

#### Staking Process

1. **Deposit Swan Tokens**:
   * Users lock Swan tokens in a secure smart contract.
   * Staking activates the accumulation of OP rewards.
2. **Daily Reward Distribution**:
   * Rewards are calculated and distributed to stakers based on their proportional stake and the day’s reward pool.
3. **Unstaking**:
   * Users can withdraw their Swan tokens and accumulated OP rewards after the staking period.

#### Reward Calculation

**Baseline TVL Growth**

The baseline TVL increases linearly from **20M Swan** to **100M Swan** over 240 days:

$$
TVL_{ ext{baseline, daily}} = 20M + \left( \frac{100M - 20M}{240} \right) \times \text{Day}
$$



**Reward Adjustments**

1.  **Daily TVL Below Baseline**:

    * A penalty multiplier $$P_m$$ applies, calculated as:

    $$P_m = 1.0 - \left( \frac{TVL_{ ext{baseline}} - TVL_{ ext{daily}}}{TVL_{ ext{baseline}}} \times 0.9 \right)$$

    * Ensures rewards reduce proportionally to TVL deficits, with a minimum multiplier of **0.1**.
2. **Daily TVL Above Baseline**:
   * A boost multiplier $$B_m = 1.2$$ applies, enhancing rewards for exceeding baseline targets.
3.  **Cap Enforcement**:

    * The total reward pool is capped at **625 OP tokens** daily:

    $$R_{ ext{final}} = \min\left(R_{ ext{adjusted}}, 625 ext{ OP tokens}\right)$$

**Individual User Rewards**

Each staker’s reward is proportional to their stake:

$$
P_{i, ext{daily}} = \frac{S_{i, ext{daily}}}{TVL_{ ext{daily}}} \times R_{ ext{final}}
$$

***

### Example Scenario

### Key Parameters <a href="#aprandrewardsystemforswanfi-keyparameters" id="aprandrewardsystemforswanfi-keyparameters"></a>

1. **Daily Base Reward**: 416.67 OP tokens.
2. **Daily Cap**: 625 OP tokens (maximum reward pool distributed daily).
3. **Baseline TVL Growth**: Linear increase from 10M Swan to 100M Swan over 240 days.
4. **Boost Multiplier**: 1.2 (reward boost for TVL above the baseline).
5. **Penalty Multiplier**: Linear adjustment from 1.0 to 0.1 based on TVL deficit.
6. **Daily TVL**: 50M Swan (below baseline).
7. **User Stake**: 5M Swan.

#### Calculations

1.  **Penalty Multiplier**:

    $$P_m = 1.0 - \left( \frac{60M - 50M}{60M} \times 0.9 \right) = 0.85$$
2.  **Adjusted Reward Pool**:

    $$R_{ ext{adjusted}} = 625 \times 0.85 =531.25  \text{ OP tokens}$$
3.  **User Reward**:

    $$P_{i, ext{daily}} = \frac{5M}{50M} \times 531.25 = 53.125 \text{ OP tokens}$$

***

### Sustainability Mechanisms

#### 1. Daily Reward Cap

* Prevents excessive distribution of OP tokens.
* Ensures the reward pool remains balanced over the program duration.

#### 2. Dynamic Multipliers

* Align rewards with TVL performance to encourage ecosystem growth.
* Penalizes underperformance while rewarding high participation.

#### 3. Locked Staking

* Encourages long-term commitment to the platform, ensuring stability.

***

### Future Enhancements

1. **Tiered Reward Structures**:
   * Introduce dynamic reward tiers to incentivize long-term stakers.
2. **Real-Time Dashboards**:
   * Provide live tracking of user rewards, staking metrics, and performance benchmarks.
3. **Cross-Platform Integration**:
   * Expand the OP reward pool model to other DePIN-compatible platforms.

***

### Conclusion

The SwanFi OP Reward Pool offers a sustainable and rewarding mechanism for Swan token holders, driving liquidity and adoption within the DePIN ecosystem. By aligning incentives with performance metrics and ensuring reward stability, SwanFi positions itself as a leader in decentralized infrastructure monetization.

***

**Stake your Swan tokens today and start earning OP rewards!**
