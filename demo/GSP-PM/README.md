# GSP-PM (Generalized Second-Price Auction based Prover Market)

## Project Overview

This research delves into the vulnerabilities present in the Prover Market of Zero-Knowledge Rollups. The prover market serves as a two-sided market connecting Layer 2 users with provers. Users require proof capacity, while provers provide it. However, this market is susceptible to attacks from both users and provers. As a result, the question of how to design a prover market to mitigate these vulnerabilities remains unanswered.

This work aims to explore the vulnerabilities in the Prover Market of Zero-Knowledge Rollups and propose a new prover market mechanism that addresses these vulnerabilities. The proposed mechanism is based on the Generalized Second-Price (GSP) auction, which allows users to bid on the computing power of provers and pay a certain amount of tokens for the computing power. The mechanism also includes a reputation system to incentivize provers with high reputation scores.

### Core Concepts
- **Staking Provers and Penalty**:
    - A prover needs to stake a certain amount of tokens (i.e., 32 ZK) to enter the prover market, which will be the initial balance of this prover. The total supply of zkSync is `21,000,000,000` ZK. A 32 ZK stake will limit the number of provers.
    - The prover's balance will increase by generating proofs for transactions and earning fees.
    - The prover's balance will decrease when not generating proofs for a period of time (i.e., 24 hours).
    - The prover's balance will be slashed when an incorrect proof is detected.
- **Second Price Bid with `BaseFee` for User Transactions**:
    - User competing for Provers via second price bidding with one time pricing. The bidding winner pay the second largest price (calculating fee) + base fee.
    - `BaseFee` here works as the reserve price for the second price auction, which is the minimum amount provers will get even users gives a very low calculating price. A high `BaseFee` means Prover capability is lacked now, and a low `BaseFee` means user transactions is not sufficient.
    - `BaseFee` is dynamically adjusted to balance the demand and supply according to the market situation.
        - If users are willing to pay a high calculation fee, it indicates that there are more user transactions than available computing power in the market. Consequently, the base fee should be adjusted higher to increase market access thresholds.
        - If the calculation fee is low, it indicates an excess of computing capacity compared to user demand. Therefore, the base fee should be lowered to accommodate more transactions in the market.

### Unclear Issues
- Is there any example of GSP auction on the blockchain?
- How to dynamically adjust the `BaseFee`?
- Do we need a reputation system in the prover market? What problems do the reputation system try to solve?

### Ongoing idea evaluation

Please refer to this [page](https://testdomaina.notion.site/OP5-Identifying-Prevent-Out-Of-Market-Malicious-Behavior-d8fb7f946e5b48d6813303bae424fca0?pvs=4) on Notion for ongoing idea evaluation.

## Team Members

[Ambition](https://github.com/AmbitionCX)

---
Many thanks to [JC](https://github.com/sun-jc), [stevending1st](https://github.com/stevending1st), and everyone else who contributed to the evaluation of this concept at the Shen Zhen Researcher House. And a special thank you to the event organizers for putting on such a fantastic and worthwhile event.
