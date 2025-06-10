# 🔐 Speaker Verification System using Voice Recognition

This mini project implements a **voice-based biometric security system** that works similarly to fingerprint or face recognition. The goal is to **verify a speaker’s identity** by analyzing their voice features.

## Objective

To design and implement a **speaker verification system** using voice recordings. The system should enroll known users and verify if a test audio sample belongs to one of them using feature comparison.

## Overview

- 🎙️ **Feature Extraction**: Uses **MFCC (Mel-Frequency Cepstral Coefficients)** to represent speaker characteristics.
- 🧠 **Verification Logic**: Compares features using **cosine similarity** to determine a match.
- ✅ **Access Decision**: If the similarity score crosses a predefined threshold, access is granted.

## Tools and Libraries

- `Python`
- `Librosa` – Audio feature extraction
- `NumPy` – Vector operations
- `Scikit-learn` – Cosine similarity & PCA
- `Matplotlib` / `Seaborn` – Data visualization

## System Workflow

1. **Enrollment Phase**  
   Extract MFCC features from known speakers' audio files and store their mean vectors.

2. **Verification Phase**  
   For new/test audio:
   - Extract MFCC features
   - Compare with enrolled data using cosine similarity
   - If similarity ≥ threshold → Access Granted

## Performance & Visualization

- **Heatmaps** of cosine similarities for test vs enrolled voices
- **MFCC Plots** showing voice patterns
- **Example Results**:
  - ✅ `anne_1.wav` matched with Anne’s profile (1.00 similarity)
  - ❌ `tom_1.wav` mismatched with Anne (0.96 similarity) → Access Denied

## Optimization

- Vectorized comparisons for faster execution
- PCA for dimensionality reduction and better clustering

## Results

- Works well for enrolled users
- Highlights importance of clear audio and well-set thresholds
- Demonstrates fundamental speaker recognition pipeline

## Conclusion

This system provides a **simple yet functional prototype** for voice-based authentication. It lays the foundation for building more robust speaker verification models using deep learning.

---

