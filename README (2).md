# 24i-2625-A2-B - The Midnight Queue (DAA Assignment 2)

Roll no: 24i-2625   Section: B   Seed s = 242625   K = 152

## Files
- 24i-2625-A2-B.ipynb / 24i-2625-A2-B.py : all code (algorithms, tests, experiments)
- results.csv : every measurement (one row per measurement)
- prediction_log.txt : prediction log written before the tournament
- README.md : this file

## How to reproduce
1. Download creditcard.csv from Kaggle (mlg-ulb/creditcardfraud). It is not included in this submission.
2. Open the notebook in Google Colab or Jupyter. Put creditcard.csv next to it (or let the notebook download it).
3. Set MODE = "full" in the settings cell (sizes 1,000 / 10,000 / 100,000 / 284,807, 5 runs, 300 s DNF limit).
4. Edit the prediction log cell, then Run all. Results are appended to results.csv, so a stopped run resumes.
5. Run the last cell to create README.md and results.csv.

## Settings
- Python 3, numpy and pandas (loading data and risk score only); no built-in sort inside any contender.
- sorted() is used only to verify outputs and to build the C3 input.
- Seed 242625, K = 25 + (242625 mod 226) = 152.
- Hardware/software: Client: HP EliteBook (7th-gen Intel Core i5), experiments run in Google Colab (VM CPU: Intel(R) Xeon(R) CPU @ 2.20GHz) | 2 logical CPUs | Python 3.13.16 | numpy 2.1.3 | pandas 2.2.3 | Linux-6.6.122+-x86_64-with-glibc2.39
- This run used MODE = quick.
