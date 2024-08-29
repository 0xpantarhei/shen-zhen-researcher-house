# OPFR (Optimistic Free Riders)

## Project Overview

This work explores the security and reliability of Optimistic Rollups, a key Layer 2 blockchain scaling solution designed to improve transaction throughput and reduce costs on the Ethereum network and other L1 blockchains. The primary focus is to determine whether validators-who are tasked with verifying the validity of transactions-will consistently perform their duties or might instead choose to act as "free riders," avoiding the costs of verification.

To address this issue, we developed a rigorous game-theoretic model that captures the strategic interactions between proposers (who submit transaction batches) and validators within the Optimistic Rollup framework. Our model specifically considers scenarios involving multiple rational validators and investigates the conditions under which these validators might choose to act honestly or default to free riding. Our analysis reveals that, in these settings, a pure strategy Nash equilibrium does not exist-meaning that validators do not uniformly engage in verification. Instead, the system tends toward a mixed strategy Nash equilibrium, where validators probabilistically decide between verifying transactions and free riding.

The implications of our findings are significant, as they suggest that in a worst-case scenario, all validators could opt to become free riders, thereby jeopardizing the security and integrity of the system. This highlights the critical need for well-designed incentive mechanisms within Optimistic Rollups to ensure that validators are sufficiently motivated to perform their roles effectively. Through our work, we contribute to the broader discourse on blockchain security by providing detailed insights into how system parameters can be optimized to minimize losses and enhance the robustness of the Optimistic Rollup mechanism. By presenting a comprehensive modelling and equilibrium analysis, we offer valuable theoretical foundations that can inform the future design and implementation of Layer 2 scaling solutions.

## Team Members

[JC](https://github.com/sun-jc), [Siyuan](https://github.com/iamliusiyuan)

## Documentation


[model.pdf](./model.pdf)
