# CSCE-635---A.I.-for-Robotics-Final-Project---Connor-Hill

# Risk-aware Safe Control for Decentralized Multi-Agent Systems

# Overview

This project takes the control framework proposed in the paper titled "Risk-aware Safe Control for Decentralized Multi-Agent Systems"
and implements it into code. After implementing the decentralized risk-aware controller, the code is then tested using the following scenarios proposed
in the paper:

Scenario 1 - Ramp Merging with 3 Vehicles
Scenario 2 - Multi-agent Position Swapping with 6 Agents

## Paper Reference

**Paper:** Risk-Aware Safe Control for Decentralized Multi-Agent Systems via Dynamic Responsibility Allocation  
**Authors:** Yiwei Lyu, Wenhao Luo, and John M. Dolan  
**Conference:** IROS 2023

## Method Implementation

The following methods/functions were implemented from the paper in order to recreate the framework's algorithm:

1.) Conditional Value at Risk using confidence level alpha
2.) Pairwise safety function
3.) Pairwise safety loss between two agents
4.) Aggregated risk for each agent
5.) Dynamical responsibility allocation
6.) Decentralized minimum safety controller
7.) Quadratic programming-based control optimization


## Repository Structure

- project_code
  - AI_Robotics_Project.ipynb
  - ai_robotics_project.py

 - results
   - scenario1_50_trial_distances.png
   - scenario1_trajectories.png
   - scenario1_pairwise_distances.png
   - scenario1_risks.png
   - scenario2_risk_aware_trajectory.png
   - scenario2_baseline_trajectory.png
   - scenario2_risk_aware_animation.mp4

- README.md

- requirements.txt


## Installation Instructions

If not already installed, install the required python packages with

pip install -r requirements.txt

NOTE:
Do this you do not already have these dependencies installed:
- numpy
- scipy
- cvxpy
- matplotlib
- ipython
- osqp
- scs

## How to Run
.ipynb file:
Run in Google Colab, Jupyter Notebook or other .ipynb compatible code software

.py file:
Download and run the following in your terminal
python ai_robotics_project.py

The following will be executed:
- The plots for Scenario 1 will be displayed
  - The distances for 50 trials
  - The pairwise distances for a single trial
  - The trajectories for a single trial
  - The total risks for a single trial
- The relevant plots for Scenario 2
  - The trajectories for the baseline controller
  - The trajectories for the risk-aware decentralized controller
- An mp4 video of the trajectories for the risk-aware decentralized controller

Note: The MP4 animation requires ffmpeg. In Google Colab, ffmpeg is usually already installed. On a local machine, install ffmpeg if the animation save step fails.



