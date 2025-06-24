# Hide-and-Shill: A Multi-Agent Reinforcement Learning Framework for Detecting Discourse-Based Market Manipulation in DeFi

![GitHub Workflow Status](https://github.com/tifoit/Hide-and-Shill/actions/workflows/main.yml/badge.svg)
![License](https://img.shields.io/github/license/tifoit/Hide-and-Shill)
![Stars](https://img.shields.io/github/stars/tifoit/Hide-and-Shill)
![Forks](https://img.shields.io/github/forks/tifoit/Hide-and-Shill)

## Introduction
"Hide-and-Shill" is a novel multi-agent reinforcement learning (MARL) framework designed to detect discourse-based market manipulation in decentralized finance (DeFi). By modeling manipulation detection as a dynamic adversarial game, this framework leverages delayed token price reactions as market-grounded reward signals to address limitations of traditional methods.

## Key Features
- **Group Relative Policy Optimization (GRPO)**: Stabilizes learning in sparse reward environments.
- **Economic Theory-Driven Reward Function**: Differentiates between fundamental value discovery and manipulation-induced noise.
- **Holistic Pipeline**: Combines LLM-extracted semantic features, social network analysis, and on-chain market data.

## Performance
Our framework demonstrates state-of-the-art (SOTA) performance in detecting subtle manipulation through analysis of 100,000 real-world discourse episodes and synthetic adversarial scenarios.

| Model               | Precision | Recall | F1-score | AUC |
|---------------------|-----------|--------|----------|-----|
| LSTM-Sentiment      | 0.68      | 0.71   | 0.69     | 0.74|
| GCN-Baseline        | 0.71      | 0.69   | 0.70     | 0.76|
| Rule-Based          | 0.55      | 0.62   | 0.58     | 0.63|
| Deepseek-Detection  | 0.72      | 0.75   | 0.73     | 0.78|
| **Hide-and-Shill**  | **0.89**  | **0.91**| **0.90** | **0.93**|

## Getting Started
### Prerequisites
- Python 3.8+
- PyTorch 2.1
- Ray RLlib
- NVIDIA CUDA 11.7+

### Installation
```bash
git clone https://github.com/tifoit/Hide-and-Shill.git
cd Hide-and-Shill
pip install -r requirements.txt
```

## Running the Framework
```bash
python main.py --mode train --config config.yaml
```

## Dataset
- **Real-World Data**: 100,000 posts and 600,000 comments from Twitter, aligned with 50 million minute-level price points from CoinGecko and Uniswap V3.
- **Synthetic Data**: 50,000 episodes generated using DeepSeek-32B.

## Documentation
- [Framework Architecture](docs/architecture.md)
- [API Reference](docs/api.md)

