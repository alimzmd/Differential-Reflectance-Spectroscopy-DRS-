README
# Differential Reflectance Spectroscopy (DRS) Analysis

An open-source data processing and analysis pipeline for **Differential Reflectance Spectroscopy (DRS)**. This project provides tools to ingest raw optical reflectance data, calculate differential spectra ($\Delta R/R$), and extract critical material properties such as bandgaps, excitonic transitions, or thin-film thicknesses.

---

## 📋 Overview

Differential Reflectance Spectroscopy is a highly sensitive, non-destructive optical technique used to characterize the electronic and structural properties of materials (especially 2D materials, thin films, and semiconductors). 

By measuring the normalized difference in reflectance between a sample and a reference substrate, this pipeline accentuates weak optical transitions that are otherwise buried in standard reflectance measurements.

### Key Formula
The core calculation performed by this software is:

$$\frac{\Delta R}{R} = \frac{R_{\text{sample}}(\lambda) - R_{\text{reference}}(\lambda)}{R_{\text{reference}}(\lambda)}$$

Where:
*   $R_{\text{sample}}(\lambda)$ is the reflectance spectrum of the material on the substrate.
*   $R_{\text{reference}}(\lambda)$ is the reflectance spectrum of the bare substrate.

---

## ✨ Features

*   **Data Ingestion:** Supports `.txt`, `.csv`, and `.dat` files exported from standard spectrometers.
*   **Baseline Correction & Smoothing:** Integrated Savitzky-Golay filtering and polynomial baseline fitting to minimize experimental noise.
*   **Automatic Derivative Analysis:** Computes first and second derivatives ($d(\Delta R/R)/dE$) to precisely locate excitonic peaks and critical points.
*   **Visualization:** Generates publication-ready plots of raw reflectance, differential reflectance, and derivative spectra.

---

## 🚀 Getting Started

### Prerequisites

Ensure you have Python 3.8+ installed. The pipeline relies on the following scientific computing libraries:

```bash
pip install numpy scipy pandas matplotlib
