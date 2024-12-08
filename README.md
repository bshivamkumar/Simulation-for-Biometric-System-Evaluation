# Simulation-for-Biometric-System-Evaluation
When designing a biometric identification system, an important aspect of the system is the capacity of the system. Designed and implemented confidence bounds using statistical programming techniques.

## Overview
This project explores the Random Match Probability (RMP) in biometric identification systems. It evaluates methods for estimating RMP and their respective upper confidence bounds (UCBs) to ensure system accuracy. The project employs Monte Carlo simulations to compare the effectiveness of three different approaches for constructing UCBs under equal and unequal probability assumptions.

## Motivation
Biometric identification systems provide secure alternatives to traditional methods such as cards, keys, or PINs by utilizing unique traits like fingerprints, facial recognition, and iris scans. However, as the number of comparisons increases, so does the likelihood of error. The RMP measures the probability of mistakenly identifying two different profiles as the same person. A lower RMP signifies higher system accuracy.

This project focuses on analyzing and improving the RMP by developing robust upper confidence bounds for its estimation.

## Goals
Assess the RMP using three distinct methods for constructing UCBs:
UB1: Binomial Assumption
UB2: Independent Comparisons Binomial Assumption
UB3: U-Statistic Approach
Compare these methods under equal and unequal probability scenarios.
Identify the most effective UCB method based on accuracy, coverage probability, and computational efficiency.

## Methodology
Monte Carlo Simulations:
Simulations are conducted to estimate the RMP and UCBs under various scenarios.
Approaches for UCB Construction:
UB1: Based on binomial distribution with 90% confidence intervals.
UB2: Assumes independence between comparisons, akin to flipping a series of coins.
UB3: Employs U-statistics for large datasets, enabling symmetric operations on data pairs for refined estimation.

## Findings
For equal probabilities:
UB1 was the most accurate, achieving the closest coverage probability to 0.95 with the lowest upper bound.
UB2 provided the highest upper bounds and near 100% coverage, making it less efficient.
UB3 performed similarly to UB1 but with slightly less precision.
For unequal probabilities:
UB3 achieved the closest coverage probability to 0.95, making it the recommended approach.

## Conclusions
Equal Probabilities: Use UB1 for its balance of precision and coverage probability.
Unequal Probabilities: Use UB3 for superior accuracy and coverage.
Recommendation: Biometric systems should adopt the method best suited to their underlying probability assumptions for optimal RMP estimation.

## References
This project relies on theoretical frameworks and studies from key publications, including:

Baumer, B., Kaplan, D., & Horton, N. Modern Data Science with R.
Harrison, R. L. Introduction to Monte Carlo Simulation.
National Research Council. The Evaluation of Forensic DNA Evidence.
