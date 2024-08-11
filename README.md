
# RL Policy Ensemble for Stock Trading

## Overview

This project explores the application of an ensemble of deep Reinforcement Learning (RL) models to optimize stock trading strategies. By integrating various RL algorithms, such as DQN, DDPG, A2C, and PPO, the project aims to create a robust trading strategy capable of navigating volatile financial markets. The ensemble approach employs a novel voting system that adjusts the influence of each model based on its performance, aiming to outperform a simple intuitive baseline.

## Key Features

- **Ensemble of RL Models**: Combines Deep Q-Networks (DQN), Deep Deterministic Policy Gradient (DDPG), Advantage Actor-Critic (A2C), and Proximal Policy Optimization (PPO) to enhance trading strategy robustness.
- **Voting Systems**: Implements two voting strategies—Max Voting and Converted Majority Thresholding—to aggregate actions from multiple agents.
- **Custom Stock Trading Simulator**: Utilizes a custom-built simulator based on OpenAI Gym, specifically designed for Apple stock (AAPL).
- **Reward Design**: Incorporates profit, holding costs, and risk penalties into the reward function to encourage stable and profitable trading.

## Project Structure

- **`data`**: Contains the adjusted closing prices and inflation adjusted prices used for training and testing.
- **`agents`**: Includes the RL agents (DQN, DDPG, A2C, PPO) with hyperparameters optimized for the experiments.
- **`simulator`**: Custom stock trading environment built using OpenAI Gym.
- **`ensemble`**: Implements Max Voting and Converted Majority Thresholding ensemble strategies.
- **`evaluation`**: Scripts to evaluate the performance of individual agents and the ensemble strategy.

## Methodology

1. **Problem Motivation**: Addressing the need for sophisticated models in the non-linear and volatile financial market.
2. **Model Ensemble**: Integrating multiple RL models into an ensemble to enhance decision-making robustness.
3. **Reward Design**: Developing a reward function that factors in profit, holding costs, and risk penalties to stabilize training.
4. **Baseline Method**: Comparing the ensemble strategy against a simple momentum-based trading strategy to assess performance gains.

## Experiments and Results

- **Initial Experiments**: Tested the agents with basic reward designs, leading to the realization that the reward scaling was inadequate.
- **Refined Reward Design**: Adjusted the reward function to penalize losses more effectively, resulting in improved agent performance.
- **Final Results**: The Converted Majority Thresholding ensemble outperformed the baseline method and individual agents, demonstrating the effectiveness of the ensemble approach in volatile markets.

## Contributions

- **Ananya Kulshrestha**: Developed the DQN and DDPG agents, preprocessed the data, implemented the custom environment, and refined the ensemble strategy.
- **David Chaudhari**: Developed the A2C and PPO agents, wrote the baseline algorithm, and contributed to the Max Voting ensemble implementation.
- **Joint Contributions**: Both team members collaborated on experiment design, presentation, and the final report.

## Conclusion

The ensemble strategy, particularly the Converted Majority Thresholding approach, proved to be effective in optimizing stock trading strategies in a volatile market. The project highlights the importance of reward design and experimentation in developing robust RL-based trading systems.

## Future Work

- **Parameter Tuning**: Further optimization of agent parameters could lead to improved performance.
- **Ensemble Strategy**: Explore dynamic weighting of agents within the ensemble based on real-time performance.
- **Environment Complexity**: Introduce additional market factors, such as random turbulence or expanded action space, to better simulate real-world conditions.

## Acknowledgements

Special thanks to the 6.8200 course staff for their support and guidance throughout this project, and a particular appreciation to Professor Agarwal for teaching the techniques that made this work possible.

## References

The project references relevant works on RL models, ensemble strategies, and stock trading simulations. For detailed citations, refer to the project paper.
