# Credit Card Fraud Detection System

## Overview

This project builds a real-world fraud detection system using behavioral
analytics and machine learning to detect fraudulent transactions while
minimizing customer inconvenience.

## Problem Statement

Financial institutions face highly imbalanced fraud datasets where less
than 1% of transactions are fraudulent but cause significant losses. The
goal is to detect fraud efficiently while reducing false positives.

## Dataset

-   Transactional data with timestamp, customer ID, terminal ID, amount
-   Highly imbalanced dataset (\<1% fraud cases)

## Feature Engineering

-   Customer behavior (24h rolling features)
-   Time-based features (hour, weekday)
-   Terminal risk features (7-day fraud rate)

## Model

-   Pipeline: StandardScaler → SMOTE → XGBoost
-   Metric: PR-AUC (best for imbalanced data)

## Results

-   PR-AUC: 0.935
-   Recall: 82.6%
-   Precision: 89.6%
-   Fraud loss prevented: \~89%

## Risk Engine

-   High Risk → Block
-   Medium Risk → OTP
-   Low Risk → Allow

## Impact

-   88.7% fraud detected in top 1% transactions
-   Customer inconvenience: 0.18%

## Future Work

-   Real-time deployment
-   Graph-based fraud detection
-   Adaptive learning
