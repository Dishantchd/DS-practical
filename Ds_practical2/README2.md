# Practical 2: Understanding Foundations of Statistics Using the Teaching Ratings Dataset

An exploratory data analysis (EDA) and descriptive statistics notebook (`DSpractical2.ipynb`) built in Python/Google Colab to examine instructor evaluations, demographics, beauty scores, and tenure status using the `TeachingRatings.csv` dataset.

## Overview

This practical covers fundamental statistical concepts and exploratory techniques in Python:

- Inspecting dataset structure, data types, and missing values
- Identifying dataset type (cross-sectional vs. time-series)
- Computing central tendency and dispersion metrics (`mean`, `median`, `min`, `max`, `std`)
- Visualizing distributions with histograms
- Comparing group-level statistics using `groupby` aggregations
- Analyzing categorical relationships using cross-tabulations (`pd.crosstab`)

## Dataset Summary

- **File:** `TeachingRatings.csv` (loaded from `/content/TeachingRatings.csv` in Colab)
- **Shape:** 463 rows × 13 columns (463 non-null entries per column; no missing values)
- **Dataset Type:** **Cross-sectional** — captures observations across 94 unique professors (`prof` IDs `1`–`94`) and courses at a single point in time rather than tracking individuals over multiple time periods.

### Columns

| Column | Data Type | Description / Observed Values |
| :--- | :--- | :--- |
| `rownames` | `int64` | Row index (`1` to `463`) |
| `minority` | `object` | Minority status (`yes`, `no`) |
| `age` | `int64` | Instructor age (`29` to `73`, mean `48.37`) |
| `gender` | `object` | Instructor gender (`female`, `male`) |
| `credits` | `object` | Course credit type (`more`, `single`) |
| `beauty` | `float64` | Standardized beauty rating (`-1.4505` to `1.9700`) |
| `eval` | `float64` | Course evaluation score (`2.1` to `5.0`, mean `4.00`) |
| `division` | `object` | Course division (`upper`, `lower`) |
| `native` | `object` | Native English speaker (`yes`, `no`) |
| `tenure` | `object` | Tenure status (`yes`, `no`) |
| `students` | `int64` | Number of students completing evaluations (`5` to `380`) |
| `allstudents` | `int64` | Total students enrolled (`8` to `581`) |
| `prof` | `int64` | Unique professor identifier (`1` to `94`) |

## Key Findings

### 1. Student Evaluation Counts (`students`)
- **Mean:** `36.62`
- **Median:** `23.0`
- **Minimum:** `5`
- **Maximum:** `380`

### 2. Beauty Scores by Gender
- **Female instructors:** Mean = `0.1161`, Standard Deviation = `0.8178`
- **Male instructors:** Mean = `-0.0845`, Standard Deviation = `0.7571`
- Female instructors have a slightly higher average beauty score and slightly higher variability than male instructors in this dataset.

### 3. Tenure Status by Gender

| Gender | Not Tenured (`no`) | Tenured (`yes`) | Tenured (%) |
| :--- | :---: | :---: | :---: |
| **Female** | 50 | 145 | 74.36% |
| **Male** | 52 | 216 | 80.60% |

A higher percentage of male instructors hold tenure (`80.60%`) compared to female instructors (`74.36%`). A formal hypothesis test (such as a Chi-Square test) would be required to determine whether this difference is statistically significant.

## Requirements

- Python 3.x
- `pandas`
- `numpy`
- `matplotlib`

Install dependencies if running locally:

```bash
pip install pandas numpy matplotlib jupyter
```

## How to Run

1. Clone or download this repository and place `TeachingRatings.csv` in your working directory (or upload it to `/content/TeachingRatings.csv` if using Google Colab).
2. If running locally, update the file path in cell 2 of `DSpractical2.ipynb`:
   ```python
   df = pd.read_csv("TeachingRatings.csv")
   ```
3. Launch Jupyter Notebook or open `DSpractical2.ipynb` in Google Colab and run all cells:
   ```bash
   jupyter notebook DSpractical2.ipynb
   ```

## Repository Structure

```text
.
├── DSpractical2.ipynb      # Main analysis notebook
├── TeachingRatings.csv     # Input dataset (required to run)
└── README.md               # Project documentation
```
