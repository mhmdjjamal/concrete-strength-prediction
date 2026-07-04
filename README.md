# Concrete Compressive Strength Prediction

An AI + Civil Engineering project predicting the compressive strength of concrete
(in MPa) from its mix design — cement, water, aggregates, and curing age — using
machine learning.

## Why this project
Concrete strength is a nonlinear function of its ingredients: cement and water
don't just add up independently, they interact. This project compares a simple
Linear Regression baseline against a Random Forest model to capture that
nonlinearity, using a real dataset of 1,030 lab-tested concrete samples
(Yeh, 1998 / UCI Machine Learning Repository).

## Results
| Model | R² | MAE |
|---|---|---|
| Linear Regression | 0.628 | 7.75 MPa |
| Random Forest | 0.881 | 3.79 MPa |

The Random Forest explains 88% of the variation in strength versus 63% for the
linear baseline, roughly halving the average prediction error. Feature importance
shows **age** and **cement** as the two strongest predictors, together accounting
for about two-thirds of the model's decisions — consistent with established
concrete theory.

## Tools
Python, pandas, scikit-learn, matplotlib — run in Google Colab.

## Dataset
[UCI Machine Learning Repository — Concrete Compressive Strength](https://archive.ics.uci.edu/dataset/165/concrete+compressive+strength)
(I-Cheng Yeh, 1998)
