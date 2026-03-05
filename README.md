# Galaxy Transition Analysis

A data analysis project exploring how galaxies transition from actively forming stars to becoming "quiescent" (no longer forming stars). This project was completed as part of my Computer Science coursework to practice data analysis and visualization skills.

---

## What This Project Does

This analysis classifies galaxies based on their star formation activity and investigates patterns in their properties:

### Galaxy Classification
Categorizes galaxies as star-forming, quiescent, AGN (active galactic nucleus), or composite

### Mass Analysis
Examines how the fraction of quiescent galaxies changes with stellar mass

### Transition Phase Discovery
Identifies galaxies in transition from star-forming to quiescent by finding outliers with bulge-dominated morphologies but ongoing star formation

---

## Key Findings

- **Higher-mass galaxies are more likely to be quiescent**
- **Star-forming galaxies with bulge-dominated structures** (Sersic N > 3) likely represent galaxies in transition from active star formation to quiescence
- **Transition phase galaxies show intermediate properties**: they still have detectable star formation (Hα emission) but are developing the structural features typical of quiescent galaxies
- **The BPT diagram effectively separates** different galaxy types when spectroscopic data is available

---

## Technical Approach

### Classification Method

#### Primary Method: BPT Diagram
Uses emission line ratios to classify galaxies
- Compares [NII]/Hα vs [OIII]/Hβ ratios
- Applies Kauffmann and Kewley demarcation lines

#### Fallback Method
For galaxies without complete spectroscopic data
- Uses D4000 index (indicator of stellar population age)
- Checks Hα emission (indicator of star formation)

### Data Processing

- Handles missing values (astronomy datasets often use -9999 as a sentinel value)
- Calculates signal-to-noise ratios for emission lines
- Bins galaxies by mass for statistical analysis

---

## Visualizations Generated

### 1. Quiescent Fraction vs Stellar Mass
Shows how galaxy properties correlate with mass

### 2. Sersic Index Comparison
Compares structural properties of star-forming vs quiescent galaxies

### 3. D4000 Distribution
Examines stellar population ages in unusual galaxies

### 4. Scatter Plots
Explore relationships between mass, D4000, and star formation activity

###Data
to get the data run : from astroML.datasets import fetch_nasa_atlas
