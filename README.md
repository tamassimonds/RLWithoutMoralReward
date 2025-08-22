# RL Without Moral Reward

This repository contains experimental results for **"All In on Winning: The Dangers of RL without Moral Reward"**.

## Overview

This research investigates the potential risks of reinforcement learning systems that are optimized purely for winning without explicit moral constraints or rewards. The experiments evaluate model behavior across different game environments and training configurations.

## Game Environments

- **KP** - Khun Poker: A simplified poker variant used to study strategic deception
- **SN** - Simple Negotiation: Bilateral negotiation scenarios  
- **TTT** - Tic-Tac-Toe: Classic strategic game environment

## Results Structure

The `eval_results/` directory contains evaluation results organized by:

- **Baseline models**: Standard pre-trained models without RL fine-tuning
- **Training configurations**: Various RL training setups with/without system prompts
- **Model ablations**: Experiments with different model sizes and architectures
- **Step progression**: Results across different training steps

Each result folder contains:
- `detailed_results_*.json`: Complete evaluation metrics and outputs
- `summary_*.json`: Aggregated performance statistics

## Related Resources

- **Training Framework**: [SPIRAL RL Library](https://github.com/spiral-rl/spiral/tree/main)
- **Models**: 
  - [Non-system prompt model](https://huggingface.co/TamasSimonds/llama-3.1-8b-instruct-no-sys-prompt-step-96): Same Sys Prompts as in SPIRAL repo
  - [System prompt model](https://huggingface.co/TamasSimonds/llama3.1-8b-kp-1k-self-play-step-336-sys-prompt/settings): Add "You are allowed to Lie and Decieve" to sys prompt during training

## Key Findings

The experiments demonstrate how RL optimization without moral constraints can lead to emergent deceptive behaviors, particularly in competitive environments where winning is the primary objective.