### Project 579 - Summary

#### Purpose
The project simulates queuing systems to analyze customer waiting times under various scheduling policies, including:
1. **Join-the-Shortest-Queue (JSQ)**: Customers join the queue with the least load.
2. **Power-of-Two-Choices (POTC)**: Customers choose the shorter of two randomly selected queues.
3. **Uniform-Random**: Customers are distributed randomly across queues.

The project aims to evaluate the performance of these policies, focusing on:
- Customer waiting times.
- Busy periods.
- Complementary Cumulative Distribution Functions (CCDFs).

#### Implementation
The project provides simulations in  **Python** with a focus on:
- **M/M/1 Queue Simulation**:
  - Models single-server systems with exponential inter-arrival and service times.
  - Analyzes system state variables like customers in the system (\(X\)), departures (\(D\)), and busy periods (\(B\)).
- **M/M/x Queues**:
  - Extends to multi-server systems (x queues).
  - Tests scheduling policies and calculates total waiting times for various arrival rates (\(\lambda\)) and service rates (\(\mu\)).

#### Features
- **Simulation Parameters**:
  - Total arrivals (\(N\)): 10,000 to 50,000.
  - Independent runs (\(K\)): 10.
  - Service rate (\(\mu\)): 1.
  - Arrival rates (\(\lambda\)): [0.7, 0.8, 0.9, 0.95] for single-server and [7, 8, 9, 9.5] for multi-server.

- **Performance Metrics**:
  - CCDFs for waiting times, departures, and busy periods.
  - Comparison of simulation results with theoretical values.

- **Visualization**:
  - CCDF plots to highlight the effectiveness of each scheduling policy.

#### Observations
1. **JSQ** consistently minimizes waiting times, making it ideal for service optimization.
2. **POTC** balances efficiency and computational simplicity, especially in large-scale systems.
3. **Uniform-Random** provides simplicity but results in higher waiting times.

#### Recommendations
- **JSQ** for environments prioritizing speed and efficiency.
- **POTC** for scalable systems with limited computational resources.
- Explore **adaptive policies** or **machine learning** for real-time queue optimization in dynamic conditions. 

This project is suitable for analyzing queuing performance in cloud services, server farms, or customer service operations.
