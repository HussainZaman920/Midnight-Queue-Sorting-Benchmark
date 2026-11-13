# Midnight-Queue-Sorting-Benchmark

Benchmarking Insertion, Merge, Quick (naive and hardened) and Heap Sort, plus top-K selection and live-feed strategies, on 284,807 credit card transactions ranked by a risk-band triage order. Includes comparison/move counting, runtime experiments across six input conditions, and recurrence analysis. Written in Python.

**24i-2625-A2-B - The Midnight Queue (DAA Assignment 2)**
Roll no: 24i-2625 | Section: B | Seed s = 242625 | K = 152

## Files
- `24i-2625-A2-B.ipynb` : all code (algorithms, tests, experiments)
- `results.csv` : every measurement (one row per measurement)
- `creditcard.csv` : dataset (via Git LFS)
- `docs/24i-2625-A2-B.pdf` : final report (Problems A-H)
- `docs/The_Midnight_Queue_Assignment_2.pdf` : assignment problem statement
- `README.md` : this file

## How to reproduce
1. `creditcard.csv` (Credit Card Fraud Detection, ULB Machine Learning Group) is included in this repository via Git LFS. Source: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud. If you clone without Git LFS, download it from Kaggle and place it next to the notebook.
2. Open the notebook in Google Colab or Jupyter. Put `creditcard.csv` next to it (or let the notebook download it).
3. Set `MODE = "full"` in the settings cell (sizes 1,000 / 10,000 / 100,000 / 284,807, 5 runs, 300 s DNF limit).
4. Edit the prediction log cell, then Run all. Results are appended to `results.csv`, so a stopped run resumes.
5. Run the last cell to regenerate the README and `results.csv`.

## Settings
- Python 3, numpy and pandas (loading data and risk score only); no built-in sort inside any contender.
- `sorted()` is used only to verify outputs and to build the C3 input.
- Seed 242625, K = 25 + (242625 mod 226) = 152.
- Hardware/software: Client: HP EliteBook (7th-gen Intel Core i5), experiments run in Google Colab (VM CPU: Intel(R) Xeon(R) CPU @ 2.20GHz) | 2 logical CPUs | Python 3.13.16 | numpy 2.1.3 | pandas 2.2.3 | Linux-6.6.122+-x86_64-with-glibc2.39

## Notes on the committed results
- The committed `results.csv` and report figures come from `MODE = quick` (n = 1,000 and 5,000 for Problem C; n = 10,000 and 50,000 for D; n = 50,000 for E). Set `MODE = "full"` to reproduce the full-size grid.
- Problem G (change request addendum) is not included in this submission.

## Dataset credit
Credit Card Fraud Detection dataset by the ULB Machine Learning Group, hosted on Kaggle. Check the licence terms on the Kaggle page before reuse.
