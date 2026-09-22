
# Healthcare Analytics for Doctor Visits

## 📌 Project Overview
This project analyses health survey data to understand what actually drives the number of doctor visits — testing common assumptions about insurance, income, and access to care against real evidence.

## 📂 Files in this Repository
| File | Description |
|---|---|
| `healthcare_data.csv` | Raw dataset — 5,190 individuals from an Australian health survey |
| `Healthcare_Analytics_Doctor_Visits.ipynb` | Jupyter Notebook containing the full analysis, code, and visualizations |
| `README.md` | Project documentation (this file) |

## 📊 Dataset Description
The dataset contains **5,190 records** covering:
- **`visits`** — number of doctor visits in a two-week reference period
- **Demographics** — gender, age (rescaled to years)
- **Economic** — income (rescaled to dollars)
- **Health status** — number of illnesses, reduced-activity days, general health score
- **Insurance type** — private insurance, low-income free cover (`freepoor`), elderly/veteran free cover (`freerepat`)
- **Chronic conditions** — non-limiting (`nchronic`) and limiting (`lchronic`) chronic condition flags

## ❓ Problem Statement
Healthcare providers and policymakers often assume that expanding insurance coverage automatically increases access to care. This project investigates which factors — insurance type, income, chronic conditions, or demographics — actually predict doctor visits, using evidence rather than assumption.

## 🔍 Analysis Performed
- Data cleaning (rescaling encoded `age`/`income` variables, outlier investigation)
- Univariate, bivariate, and multivariate analysis
- Correlation analysis across numeric health and demographic variables
- Statistical testing (t-tests, chi-square) to confirm which patterns are real vs. due to chance
- 4 student-designed deep-dive analyses:
  - Does private insurance increase visits? (insurance-access paradox)
  - Do government assistance programs behave differently?
  - What characterizes people who never visit the doctor?
  - Visit distribution shape by gender (violin plot)
- Evidence-based conclusions and recommendations

## 🛠️ Tools & Libraries Used
- Python 3
- pandas, numpy
- matplotlib, seaborn
- scipy (statistical testing)
- Jupyter Notebook

## 🚀 How to Run
1. Clone this repository:
   ```bash
   git clone <https://github.com/Charu4994/Healthcare_Analytics_Doctor_Visits/edit/main/README.md>
   ```
2. Make sure the `.csv` and `.ipynb` files are in the **same folder**.
3. Open the notebook:
   ```bash
   jupyter notebook Healthcare_Analytics_Doctor_Visits.ipynb
   ```
4. Run all cells: **Kernel → Restart & Run All**.

## 🔑 Key Insights
- **Having a limiting chronic condition more than doubles average doctor visits** (0.60 vs 0.26) — the strongest single predictor found.
- **Private insurance shows no measurable effect on visit frequency** (p = 0.57) — explained by a "healthy user" selection effect: privately insured individuals are wealthier and healthier on average.
- **Government insurance programs diverge sharply**: `freerepat` (elderly/veteran cover) is linked to far more visits, while `freepoor` (low-income cover) is linked to fewer visits — suggesting non-financial barriers persist for low-income individuals despite free coverage.
- **Women visit the doctor significantly more than men** (p < 0.0001), and a genuinely larger share of women visit at all (40% vs 30%), not just a few frequent visitors.
- **~80% of individuals had zero doctor visits** in the two-week window — the data is heavily zero-inflated.

## 🙋 Author
Charu Yadav

---
*This project was completed as part of a Data Analytics case study.*
