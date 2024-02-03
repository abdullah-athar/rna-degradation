# RNA Stability Prediction Challenge - My Attempt

## Overview
This repository captures my journey and efforts to tackle the Kaggle competition focused on predicting the degradation rates of RNA molecules. The challenge aims to address crucial aspects of designing stable messenger RNA (mRNA) molecules for vaccines.

## Challenge Description

The challenge revolves around the stability of mRNA vaccines, with a specific focus on designing super-stable mRNA molecules. The key challenge lies in understanding the regions prone to degradation within RNA molecules. 

## Datasets

### Files

- **train.json**: Training data containing information on RNA sequences, their structures, and experimental values for reactivity and degradation rates.
  
- **test.json**: Test set without columns associated with ground truth. It includes sequences with longer lengths for private evaluation.

- **sample_submission.csv**: Sample submission file in the correct format for predictions.

### Columns

- **id**: Arbitrary identifier for each sample.

- **seq_scored**: Integer value denoting the number of positions used in scoring with predicted values. Matches the length of reactivity, deg_*, and *_error_* columns.

- **seq_length**: Integer values denoting the length of the sequence.

- **sequence**: String describing the RNA sequence (107 characters in Train/Public Test, 130 in Private Test).

- **structure**: String describing whether a base is estimated to be paired or unpaired.

- **reactivity**: Array of floating point numbers representing reactivity values.

- **deg_pH10**: Array of floating point numbers representing reactivity values at high pH (pH 10).

- **deg_Mg_pH10**: Array of floating point numbers representing reactivity values at high pH (pH 10) with magnesium.

- **deg_50C**: Array of floating point numbers representing reactivity values at high temperature (50 degrees Celsius).

- **deg_Mg_50C**: Array of floating point numbers representing reactivity values at high temperature (50 degrees Celsius) with magnesium.

- **_error_**: Array of floating point numbers representing errors in experimental values.

- **predicted_loop_type**: String describing the structural context (loop type) of each character in the sequence.

- **S/N filter**: Indicates if the sample passed certain filters.

### Additional Notes

- Measurements are available for the first 68 bases of 107-base sequences (Train/Public Test) and the first 91 bases of 130-base sequences (Private Test).

- The public test set (test.json) comprises 629 sequences, filtered based on certain criteria for public leaderboard scoring.

- The private test set (test.json) includes 3005 sequences with longer lengths, and the same three filters as the public test set will be applied for private leaderboard scoring.

## Model

TBD

## Getting Started

1. Clone this repository to access the code and resources used in my attempt.
2. TBD

## Evaluation

My submissions will be evaluated based on MCRMSE scores (mean columnwise root mean squared error).

