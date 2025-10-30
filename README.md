# Kalman-Filtered Trend Trader: A Deep Reinforcement Learning Agent for Portfolio Allocation

This repository is part of **WiDS (Women in Data Science)** conducted by **The Analytics Club, IIT Bombay**.

---

## Project Overview

**Problem Statement:**  
Simple "buy-and-hold" trading strategies often fail during market downturns, while overly reactive models get misled by short-term noise.  
This project aims to design an **autonomous trading agent** that makes intelligent, long-term portfolio decisions based on the *true underlying market trend* — not just daily volatility.

**Goal:**  
Build a Deep Reinforcement Learning (RL) agent that allocates between a **risky asset** (e.g., SPY ETF) and a **stable asset** (cash) to maximize portfolio value over time.

**Core Idea:**  
Instead of feeding noisy prices to the agent, use a **Kalman Filter** to estimate the true price and its trend (velocity).  
The RL agent learns an optimal policy — when to buy, sell, or hold — from these filtered signals.

---

## Key Learning Outcomes

By completing this project, you will learn:

- Reinforcement Learning fundamentals (state, action, reward, policy)
- Financial portfolio optimization and backtesting
- Kalman Filtering and state-space modeling
- Time-series noise reduction and trend estimation
- Custom Gym environment creation for trading
- Training RL agents using **Stable-Baselines3 (PPO, A2C, DDPG)**
- Performance evaluation with transaction costs and benchmarks

---

## Weekly Contents

### **Week 1 – Foundations of Financial Data & RL**
**Goal:** Build intuition for trading and RL basics.  
**Learn:**  
- Portfolio optimization, returns, and volatility  
- Python tools: `pandas`, `numpy`, `matplotlib`, `yfinance`  
- RL basics: state, action, reward, policy  
- “Buy & Hold” vs “Active” strategies  

**Deliverables:**  
- Download and visualize SPY data  
- Plot daily & cumulative returns  
- Write a short note explaining the RL loop  

---

### **Week 2 – Kalman Filter & Trend Estimation**
**Goal:** Implement a Kalman Filter to extract the true trend from noisy data.  
**Learn:**  
- Hidden-state modeling: [price, velocity]  
- Process vs measurement noise  
- Implementing Kalman Filter (`numpy` or `filterpy`)  
- Tuning parameters and visualizing results  

**Deliverables:**  
- Jupyter Notebook plotting:
  - Raw vs filtered price  
  - Estimated velocity (trend)  

---

### **Week 3 – Building the Trading Environment**
**Goal:** Create a custom environment for RL training.  
**Learn:**  
- Gymnasium API structure (`reset`, `step`, `render`)  
- Define state = [allocation, estimated_price, velocity]  
- Reward = portfolio gain – transaction cost  

**Deliverables:**  
- `portfolio_env.py`  
- Test with random actions to ensure stability  

---

### **Week 4 – Training the RL Agent**
**Goal:** Train a reinforcement learning agent using real data.  
**Learn:**  
- Using `stable-baselines3` (PPO, A2C, or DDPG)  
- Continuous action spaces  
- Model saving, loading, and evaluation  

**Deliverables:**  
- Trained RL model (e.g., `ppo_portfolio_trader.zip`)  
- Training plots showing portfolio performance  

---

### **Week 5 – Backtesting & Performance Evaluation**
**Goal:** Evaluate on unseen test data.  
**Learn:**  
- Backtesting concepts  
- Metrics: Sharpe ratio, drawdown, cumulative return  
- Compare against Buy & Hold and SPY benchmark  

**Deliverables:**  
- “Money Plot” comparing all strategies  
- Summary of results and performance insights  

---

### **Week 6 – Insights, Optimization & Presentation**
**Goal:** Finalize, analyze, and showcase your work.  
**Learn:**  
- Sensitivity to transaction costs and model parameters  
- Documentation and storytelling for projects  
- Preparing a professional README and result plots  

**Deliverables:**  
- Final GitHub repo with:
  - 📊 Money Plot  
  - 📈 Filter visualization  
  - 🧾 README.md + short project report  

---

## Final Deliverable

A **complete end-to-end system** that integrates:
[Stock Data] → [Kalman Filter] → [Trend Estimate] → [RL Agent (PPO)] → [Allocation %] → [Portfolio Value]


**Success Metric:**  
Your agent’s portfolio curve beats both **Buy & Hold** and **SPY** over unseen test data (2023–2024).

---

## Why This Project Matters

This project blends **machine learning**, **finance**, and **signal processing** into a single hands-on system.  
You’ll gain the technical and conceptual depth needed for **quantitative trading**, **AI research**, and **data-driven financial modeling** — all while learning to see through noise and act intelligently.

---

### Tools & Libraries

- Python (NumPy, Pandas, Matplotlib)
- `yfinance` for market data
- `filterpy` or manual Kalman implementation
- `gymnasium` for custom environment
- `stable-baselines3` for RL training
- `scikit-learn` for evaluation and analysis

---

### End Goal

By the end of this project, you’ll have a:
- Trained **Deep RL trading agent**  
- Functional **Kalman Filter trend estimator**  
- Fully documented **GitHub project** showcasing a data-driven portfolio optimization pipeline.

---

> *“An intelligent trading agent doesn’t just follow prices — it understands the market’s rhythm.”*
