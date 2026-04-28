# Tonal Homogeneity as a Design Principle: A Computational Analysis of Mozart's Musikalisches Würfelspiel

This repository contains the project materials and source code for our ISMIR 2026 submission. We investigate the computational design principles of Mozart's Musikalisches Würfelspiel (K. 516f), focusing on how stylistic coherence is maintained despite random selection.

## Research Overview
We investigate why Mozart's dice game produces musically coherent results despite random assembly, and identify the computational design principles that make this possible.

## Important Notice on Data Accessibility
Please note that due to copyright restrictions, the complete set of musical samples and corpora used in this study cannot be fully hosted in this public repository. Consequently, the provided source code is intended for methodological transparency and review of the analytical process, rather than for direct execution or reproduction of the results without the original dataset.

## Repository Structure

* perceptionvalidation/: Audio stimuli (.mp3) used for perceptual validation.
* mozartdice_midi/: Original MIDI samples (.mid) from the Mozart Dice system.
* musicbox_generation/:  Algorithmically generated music pieces based on the Mozart's Music Box system.
* analysis/: Python scripts and Jupyter notebooks for data analysis and music information retrieval.

## Source Code Details (analysis/)

The scripts in the `analysis/` directory document the experimental processes and results presented in the paper:

### 1. fourcomposerscomparison.ipynb
* **Paper Sections**: 
    * Section 4.1: Tonal Homogeneity
    * Section 4.2: Pitch-Class Space Clustering
    * Section 4.3: Voice Leading: The Deceptive Variety Mechanism
    * Section 4.4: Tonic Containment and Registral Dissociation
    * Section 4.7: Within-composer validation
* **Function**: Implements the core statistical analysis to establish "The Tonal Floor" and "Deceptive Variety". It calculates the tonal spread ($\sigma=0.822$) and voice-leading distances (Raw=2.143, Tymoczko=0.508) across multiple datasets. It also performs within-composer validation against 16 Mozart string quartet minuets.

### 2. listenerStudyAnalysis.ipynb
* **Paper Section**: Section 4.6: Perceptual Validation
* **Function**: Analyzes results from the online pilot study ($N=20$) to compare naturalness ratings between Mozart's dice game and control sequences. It documents that Mozart-generated excerpts were rated significantly more natural than scrambled versions ($p=0.009$).

### 3. generativevalidation.ipynb
* **Paper Sections**: 
    * Section 4.5: Structural Boundaries
    * Section 4.8: Generative Evaluation
* **Function**: Validates the generative system using G-PELT changepoint detection to verify structural uniformity at the event-graph level. It evaluates the "Mozart's Music Box" system, confirming that the tonal floor generalizes to a new instrument and source corpus ($\sigma=0.864$).


## Requirements

* Python 3.x
* music21 (Core toolkit for musicological analysis)
* pandas, numpy, matplotlib, umap-learn (For data processing and visualization)
