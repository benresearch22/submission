# Tonal Homogeneity as a Design Principle: A Computational Analysis of Mozart's Musikalisches Würfelspiel

This repository contains the project materials and source code for our ISMIR 2026 submission. We investigate the computational design principles of Mozart's Musikalisches Würfelspiel (K. 516f), focusing on how stylistic coherence is maintained despite random selection.

## Research Overview
We propose a two-factor explanation for the stylistic consistency of the dice game:
1. Tonal Floor: 88.6% of the 176 measures cluster within a narrow D-major region (sigma=0.822), significantly lower than Haydn, Beethoven, and Schubert.
2. Deceptive Variety: High registral displacement (raw distance 2.143) masking minimal pitch-class movement (Tymoczko distance 0.508).

## Important Notice on Data Accessibility
Please note that due to copyright restrictions, the complete set of musical samples and corpora used in this study cannot be fully hosted in this public repository. Consequently, the provided source code is intended for methodological transparency and review of the analytical process, rather than for direct execution or reproduction of the results without the original dataset.

## Repository Structure

* perceptionvalidation/: Audio stimuli (.mp3) used for perceptual validation.
* mozartdice_midi/: Original MIDI samples (.mid) from the Mozart Dice system.
* musicbox_generation/: AI-generated music pieces based on the Mozart Dice algorithm.
* analysis/: Python scripts and Jupyter notebooks for data analysis and music information retrieval.

## Source Code Details (analysis/)

The scripts in the analysis/ directory document the analysis and visualization processes presented in the paper:

1. listenerStudyAnalysis.ipynb
- Paper Section: Section 4.6 (Perceptual Validation)
- Function: Conducts statistical analysis on the listener study (n=20). Compares "naturalness" ratings between Mozart's generated minuets, authentic Haydn samples, and randomized baselines.

2. retestwithBeethoven.ipynb
- Paper Section: Section 4.1 (Tonal Homogeneity) and Section 4.3 (Cross-Corpus Comparison)
- Function: Processes Beethoven (Piano Sonatas and String Quartets) and Schubert datasets to calculate the tonal spread (sigma) for comparative corpus analysis.

3. generativevalidation.ipynb
- Paper Section: Section 4.7 (Generative Validation)
- Function: Validates the "Mozart's Music Box" generation system by computing statistical signatures (sigma, Voice-Leading distances) and applying G-PELT changepoint detection.

## Requirements

* Python 3.x
* music21 (Core toolkit for musicological analysis)
* pandas, numpy, matplotlib, umap-learn (For data processing and visualization)
