# Materials Band Gap Prediction & Screening

A materials informatics workflow for predicting experimental band gaps and screening semiconductor candidates using machine learning — motivated by accelerated materials discovery for functional and energy applications.

---

## Overview

Traditional materials discovery is constrained by slow trial-and-error experimentation. This project demonstrates how composition-based descriptors combined with machine learning can be used to:

- **Predict band gaps** of inorganic compounds from their elemental composition alone
- **Compare ML models** to identify the best-performing approach for this regression task
- **Screen candidate materials** by filtering predictions for semiconductor-relevant band gap ranges (~0.5–3.5 eV)

This workflow is a prototype for the kind of data-driven pipeline increasingly used in high-throughput materials research.

---

## Motivation

This project was developed to build practical experience at the intersection of **materials science and machine learning** — specifically targeting the growing demand for researchers who can bridge experimental characterization with computational screening and data-driven design.

Key research questions addressed:
1. How well can ML models predict band gaps from composition-only features?
2. Which model architectures perform best on small-to-medium materials datasets?
3. How can predictions be used to prioritize candidates for experimental investigation?

---

## Methods

### Feature Engineering
- Composition-based descriptors derived from elemental properties (atomic radius, electronegativity, ionization energy, etc.)
- Features computed using stoichiometric weighting of constituent elements

### Models Compared
| Model | Description |
|-------|-------------|
| Random Forest | Ensemble of decision trees; handles non-linear relationships well |
| Gradient Boosting | Sequential boosting; strong baseline for tabular data |
| Neural Network | Multi-layer perceptron; flexible but requires careful tuning |
| Linear Regression | Baseline reference |

### Evaluation Metrics
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² score

### Screening Pipeline
- Predictions filtered to the semiconductor window (0.5 eV – 3.5 eV)
- Candidates ranked by predicted band gap and model confidence

---

## Results

The workflow successfully identifies semiconductor candidates from composition space and demonstrates that composition-based ML can provide useful first-pass screening before costly DFT calculations or experimental synthesis.

> Full results, model comparisons, and visualizations are available in the notebook.

---

## Repository Structure

```
materials-bandgap-screening/
│
├── band_gap_prediction_.ipynb   # Main notebook: EDA, training, screening
├── README.md                    # This file
└── data/                        # Dataset files (if applicable)
```

---

## Tools & Libraries

- **Python 3**
- `pandas`, `numpy` — data handling
- `scikit-learn` — ML models and evaluation
- `matplotlib`, `seaborn` — visualization
- `matminer` (optional) — materials feature generation

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/tarekhammam73-ai/materials-bandgap-screening.git
   cd materials-bandgap-screening
   ```

2. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
   ```

3. Open the notebook:
   ```bash
   jupyter notebook band_gap_prediction_.ipynb
   ```

Or run directly in Google Colab — no local setup needed.

---

## Author

**Tarek Mohamed Mahmoud**  
Research Assistant, Kuwait Institute for Scientific Research  
M.Sc. Physics & Electronics, South Valley University  

- 📧 Tarek.hammam73@gmail.com  
- 🔗 [LinkedIn](https://www.linkedin.com/in/tarek-hammam)  
- 🔬 [ResearchGate](https://www.researchgate.net/profile/Tarek-Hammam-3)

---

## Related Work

This project complements my experimental research in thin-film optoelectronics, where I study structure–property relationships in functional materials. Bridging experimental characterization with data-driven prediction is a central goal of my PhD research trajectory.

**Publication:** [Effect of Protective Layer on the Performance of Monocrystalline Silicon Cell for Indoor Light Harvesting](https://doi.org/10.3390/s23187995) — *Sensors*, 2023.
