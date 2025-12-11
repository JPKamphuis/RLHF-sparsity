# Overview
This code explores the effect of noise in a human's feedback alongside the sparsity of feedback provided to reinforcement learning from human feedback (RLHF) models. We explore a model-based and model-free framework based on REINFORCE to find an optimal policy in an 8x8 gridworld setting.

# Environment Setup
environment.yml contains the conda environment with all packages needed to run the code. An environment can be created with ```conda env create -f environment.yml```
# Note on solver
The model-based approach uses the MOSEK solver, which requires a license. It can be replaced with a default solver from CVXPY, such as SCS.
# Running the code
The jupyter notebooks contain all the code to replicate the findings and figures in our paper.

model_free.ipynb defines the model-free REINFORCE algorithm which updates the policy with the direct human feedback

baseline(EOT)_model_based.ipynb estimates the reward function and learns from only end-of-trajectory feedback

sparse_feedback_model_based.ipynb implements the same framework as the previous notebook but samples feedback more often than end-of-trajectory.
