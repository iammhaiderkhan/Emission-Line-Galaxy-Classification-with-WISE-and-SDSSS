# Emission-Line Galaxy Classification with SDSS and WISE  

This repository contains a Jupyter Notebook developed as part of the **Active Galactic Nuclei (AGN) course project**, focused on the classification of emission-line galaxies using data from the Sloan Digital Sky Survey (SDSS) and the Wide-field Infrared Survey Explorer (WISE).  

## Project Overview  
With the increasing availability of large astronomical surveys, a major challenge is the reliable classification of galaxies with emission lines. In particular, we aim to distinguish **star-forming galaxies** from **active galactic nuclei (AGN)** using a variety of diagnostic tools.  

This project reproduces and explores several widely used classification methods, including:  
- **BPT Diagrams** (Baldwin, Phillips & Terlevich 1981) – based on optical emission line ratios.  
- **WHAN Diagram** (Cid Fernandes et al. 2011) – useful for weak emission-line galaxies and separating AGN from retired galaxies.  
- **TBT Diagram** (Trouille, Barger & Tremonti 2011) – redshift-independent classification using [NeIII]/[OII] line ratio and rest-frame colors.  
- **WISE Mid-Infrared Colors** (Mateos et al. 2012, 2013) – identifying AGN through infrared dust emission signatures.  
- **Variability Studies** – modeling AGN light curves with machine learning (Conditional Neural Processes).  

## Implemented Tasks  

### **Task 1 – SDSS Emission-Line Classification**  
- Extracted a large galaxy sample (z < 0.35) with narrow emission lines from SDSS.  
- Computed diagnostic emission-line ratios ([OIII]/Hβ, [NII]/Hα, [SII]/Hα, [OI]/Hα).  
- Constructed **BPT diagrams** with theoretical and empirical division lines.  
- Investigated cosmic evolution of BPT classifications across redshift bins.  
- Compared classifications across multiple BPT variants.  
- Built the **WHAN diagram** and compared its classifications with BPT results.  

### **Task 2 (Optional) – TBT Diagnostics**  
- Selected subsample with [NeIII] and [OII] line measurements.  
- Performed k-corrections to obtain rest-frame (g−z) colors.  
- Constructed the **TBT diagram** and compared results with BPT classifications.  

### **Task 3 – Mid-Infrared WISE Diagnostics**  
- Cross-matched SDSS AGN with WISE sources.  
- Computed MIR colors (W1, W2, W3).  
- Plotted galaxies on the **WISE color–color diagram**, applying Mateos et al. (2012) wedge selection.  
- Compared AGN classifications between optical (SDSS) and infrared (WISE) surveys.  

### **Task 4 – Variability Analysis (Optional)**  
- Extracted light curves of quasars (Type 1 AGN) from SDSS Stripe 82.  
- Modeled quasar variability using the **QNPy package** (Conditional Neural Processes).  
- Computed light curve statistics: number of points, gaps, sampling cadence, variability amplitudes.  
- Evaluated how well the models capture AGN variability patterns.  

## Requirements  
The notebook requires:  
- **Python 3**  
- Standard scientific stack: `numpy`, `scipy`, `matplotlib`, `pandas`, `astropy`  
- SDSS and WISE data access (via SQL queries or pre-downloaded tables)  
- Optional: `QNPy` for Task 4  

Install dependencies with:  
```bash
pip install -r requirements.txt
