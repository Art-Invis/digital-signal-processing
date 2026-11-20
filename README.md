# Digital Signal Processing (DSP) — Laboratory Works

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-Scientific%20Computing-013243?logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-Signal%20Processing-8CAAE6?logo=scipy&logoColor=white)
![PyWavelets](https://img.shields.io/badge/PyWavelets-Wavelet%20Analysis-orange)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557c)

A collection of laboratory works for the **Fundamentals of Digital Signal Processing** course at **Lviv Polytechnic National University** (Department of Computerized Automation Systems, *System Engineering & Internet of Things* program).

Although the original coursework specifications target MATLAB, all algorithms, analytical verifications, and visualizations in this repository are re-implemented from scratch and validated in **Python** using open-source scientific libraries (`NumPy`, `SciPy`, `PyWavelets`, and `Matplotlib`).

---

## Coursework Overview (Variant #5)

| Lab # | Topic | Key Methods & Concepts | Directory |
| :---: | :--- | :--- | :---: |
| **01** | **Function Interpolation & Approximation** | Polynomial interpolation and numerical approximation of discrete data sets | [`lab1/`](./lab1) |
| **02** | **Fourier Series & Exponential Approximation** | Periodic signal approximation via Fourier series (with Nyquist harmonic correction), Least Squares exponential fitting ($f(x) = e^{A+Bx}$) | [`lab2/`](./lab2) |
| **03** | **Discrete & Fast Fourier Transform (DFT / FFT)** | Complex spectral analysis, amplitude & phase spectra computation, $T_a$ scaling, zero-centered frequency shifting, manual vs. FFT verification | [`lab3/`](./lab3) |
| **04** | **Non-Recursive Digital Filters (FIR)** | 4th-order High-Pass Filter ($f_g = 30\text{ Hz}$, $f_a = 500\text{ Hz}$); analytical non-symmetric vs. symmetric linear-phase `firwin` design; magnitude, phase & impulse responses | [`lab4/`](./lab4) |
| **05** | **Wavelet Analysis & Signal Denoising** | 3-level DWT via Mallat's algorithm (`coif4`), `wrcoef` branch reconstruction, level-dependent MAD noise estimation (Type 2), `sqtwolog` soft thresholding | [`lab5/`](./lab5) |

---

## Engineering Highlights

* **MATLAB-to-Python Parity:** Exact functional equivalents of MATLAB Signal Processing and Wavelet Toolbox routines (`fft`, `fir1`, `freqz`, `impz`, `filter`, `waveinfo`, `wavefun`, `wfilters`, `wavedec`, `wrcoef`, `wnoisest`, `thselect`, `waverec`).
* **First-Principles Verification:** Analytical formulas are explicitly coded from scratch alongside high-level library functions to verify mathematical accuracy and inspect underlying edge cases:
  * Proper handling of the Nyquist frequency component in discrete Fourier series.
  * Direct comparison of non-symmetric analytical FIR coefficients against symmetric linear-phase implementations (`scipy.signal.firwin`).
  * Verification of Mallat's perfect reconstruction identity $\max |S - (A_3 + D_3 + D_2 + D_1)| \approx 10^{-14}$ prior to thresholding.
* **Comprehensive Visualization:** Multi-panel plots illustrating time-domain signals, frequency/phase responses, impulse characteristics, filter banks, thresholding corridors ($\pm \tau_j$), and extracted noise components.

---

## Repository Structure

```text
digital-signal-processing/
├── lab1/                   # Function Interpolation & Approximation
├── lab2/                   # Periodic (Fourier) & Exponential Approximation
├── lab3/                   # DFT & FFT Spectral Analysis
├── lab4/                   # Non-Recursive FIR High-Pass Filter Design
│   ├── lab_4_task.ipynb
│   ├── lab4_plots.png
│   └── README.md
├── lab5/                   # Discrete Wavelet Transform & Denoising (coif4)
│   ├── Lab_3_5.mat
│   ├── lab_5_task.ipynb
│   ├── lab5_1_wavelet_info.png
│   ├── lab5_2_decomposition_tree.png
│   ├── lab5_3_thresholding_levels.png
│   ├── lab5_4_final_denoising.png
│   └── README.md
└── README.md
```

---

## Getting Started

### Prerequisites
* **Python 3.8+**
* Optional: **Jupyter Notebook** or **Google Colab**

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Art-Invis/digital-signal-processing.git
   cd digital-signal-processing
   ```

2. Install the required dependencies:
   ```bash
   pip install numpy scipy matplotlib PyWavelets
   ```

3. Navigate into any laboratory directory and run the corresponding script:
   ```bash
   cd lab5
   python lab5_task.ipynb
   ```

---

## Author

**Artem** — Computer Science (System Engineering & IoT) Student, Lviv Polytechnic National University.