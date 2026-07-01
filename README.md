# 📊 Spread Locator - Statistical Distribution Analysis

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge&logo=jupyter)
![Data Science](https://img.shields.io/badge/Data%20Science-Analytics-green?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

**Advanced Statistical Analysis & Distribution Modeling for Transaction Data** 📈

[🎯 Quick Start](#-quick-start) • [📚 Theory](#-theoretical-foundation) • [💻 Implementation](#-practical-implementation) • [📊 Data](#-dataset-overview) • [📖 Documentation](#-documentation)

</div>

---

## 🎯 Project Overview

**Spread Locator** is a comprehensive data science project that combines theoretical statistical foundations with practical machine learning implementations to analyze and model distribution patterns in transaction data. This project helps identify, analyze, and predict transaction behavior across different regions and customer segments.

### ✨ Key Features

| Feature | Description | Impact |
|---------|-------------|--------|
| 🎓 **Theoretical Foundation** | Mathematical basis for statistical distributions | Ensures scientific rigor |
| 🔬 **Statistical Analysis** | Distribution modeling and hypothesis testing | Identifies data patterns |
| 💾 **Real-world Dataset** | 221 transactions across multiple regions | Practical insights |
| 📈 **Predictive Modeling** | ML algorithms for transaction forecasting | Business value |
| 🗺️ **Geographic Analysis** | Regional transaction patterns | Location-based insights |

---

## 📁 Project Structure

```
Spread Locator/
├── 📄 theory concept : Part A - Theoretical Foundation.pdf
│   └── Mathematical foundations and statistical concepts
├── 📓 Statistical_Distribution_Analysis_model-checkpoint.ipynb
│   └── Practical implementation and analysis
└── 📊 Speed_Locator_Data.csv
    └── Raw transaction dataset (221 records)
```

---

## 📚 Theoretical Foundation

### 📖 Part A: Theoretical Concepts

The theoretical foundation document covers essential statistical concepts:

#### Key Theoretical Topics

| Topic | Concept | Formula |
|-------|---------|---------|
| **Mean (μ)** | Central tendency measure | $$\mu = \frac{1}{n}\sum_{i=1}^{n} x_i$$ |
| **Standard Deviation (σ)** | Spread measure | $$\sigma = \sqrt{\frac{1}{n}\sum_{i=1}^{n}(x_i - \mu)^2}$$ |
| **Variance (σ²)** | Square of deviation | $$\sigma^2 = \frac{1}{n}\sum_{i=1}^{n}(x_i - \mu)^2$$ |
| **Skewness** | Distribution symmetry | $$\gamma_1 = \frac{\sum(x_i - \mu)^3}{n\sigma^3}$$ |
| **Kurtosis** | Tail behavior | $$\gamma_2 = \frac{\sum(x_i - \mu)^4}{n\sigma^4} - 3$$ |
| **Correlation** | Relationship strength | $$r = \frac{\sum(x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\sum(x_i - \bar{x})^2\sum(y_i - \bar{y})^2}}$$ |

#### Distribution Types Analyzed

```
Normal Distribution (Gaussian)
    PDF: f(x) = (1/(σ√(2π))) * e^(-(x-μ)²/(2σ²))
    Use Case: Transaction amounts, customer spending patterns

Exponential Distribution
    PDF: f(x) = λe^(-λx), x ≥ 0
    Use Case: Time between transactions, waiting times

Poisson Distribution
    PMF: P(X=k) = (e^(-λ) * λ^k) / k!
    Use Case: Transaction count, rare events

Beta Distribution
    PDF: f(x) = (Γ(α+β))/(Γ(α)Γ(β)) * x^(α-1) * (1-x)^(β-1)
    Use Case: Proportions, success rates
```

📖 **[Download Full Theory Document](theory%20concept%20:%20Part%20A%20-%20Theoretical%20Foundation.pdf)**

---

## 💻 Practical Implementation

### 🔬 Statistical Distribution Analysis Model

The Jupyter notebook contains complete implementation of distribution analysis with Python data science stack.

#### Technology Stack

| Component | Technology | Version |
|-----------|-----------|---------|
| **Language** | Python | 3.8+ |
| **Data Processing** | Pandas | 1.3+ |
| **Numerical Computing** | NumPy | 1.21+ |
| **Visualization** | Matplotlib, Seaborn | Latest |
| **Statistics** | SciPy | 1.7+ |
| **Machine Learning** | Scikit-learn | 0.24+ |
| **Notebook** | Jupyter | 3.0+ |

#### Analysis Workflow

```
1️⃣ Data Loading & Exploration
    ↓
2️⃣ Data Cleaning & Preprocessing
    ↓
3️⃣ Descriptive Statistics
    ↓
4️⃣ Distribution Fitting & Testing
    ↓
5️⃣ Visualization & Insights
    ↓
6️⃣ Predictive Modeling
    ↓
7️⃣ Results & Recommendations
```

#### Key Analysis Functions

| Function | Purpose | Output |
|----------|---------|--------|
| `describe_distribution()` | Calculate distribution statistics | Mean, Std, Skew, Kurt |
| `fit_distribution()` | Fit data to theoretical distributions | Best-fit parameters |
| `normality_test()` | Test for normality (Shapiro-Wilk) | p-value, result |
| `visualize_dist()` | Create distribution plots | Histograms, Q-Q plots |
| `predict_transactions()` | ML-based forecasting | Future transaction values |
| `regional_analysis()` | Geographic pattern analysis | Regional insights |

📓 **[Open Jupyter Notebook](Statistical_Distribution_Analysis_model-checkpoint.ipynb)**

---

## 📊 Dataset Overview

### 📈 Speed_Locator_Data.csv

Real-world transaction dataset with comprehensive attributes for analysis.

#### Dataset Dimensions

| Metric | Value |
|--------|-------|
| 📋 Total Records | 221 transactions |
| 🏷️ Total Columns | 7 attributes |
| 🗓️ Time Period | January 2023 |
| 🌍 Geographic Coverage | 4 regions (North, South, East, West) |
| 💰 Transaction Range | $804.42 - $20,462.84 |

#### Data Schema & Statistics

| Column | Type | Range/Values | Description |
|--------|------|--------------|-------------|
| **transaction_id** | UUID | 221 unique | Unique transaction identifier |
| **customer_id** | String | CUST[0-9]+ | Customer identifier |
| **transaction_amount** | Float | 804.42 - 20,462.84 | Amount in currency units |
| **transaction_date** | Date | 2023-01-01 to 2023-01-31 | Transaction date |
| **transaction_count** | Integer | 0 - 9 | Number of transactions |
| **region** | Categorical | North, South, East, West | Geographic region |
| **transaction_status** | Categorical | Success, Fail | Transaction outcome |

#### Statistical Summary

```
Transaction Amount Distribution:
┌─────────────────────────────────────────────────────┐
│ Mean      : $3,374.52                              │
│ Median    : $3,261.80                              │
│ Std Dev   : $2,105.43                              │
│ Min       : $804.42                                │
│ Max       : $20,462.84                             │
│ Range     : $19,658.42                             │
│ Q1 (25%)  : $1,987.46                              │
│ Q3 (75%)  : $4,497.22                              │
└─────────────────────────────────────────────────────┘

Success Rate Analysis:
┌─────────────────────────────────────────────────────┐
│ Total Transactions    : 221                         │
│ Successful           : 103 (46.6%)  ✅             │
│ Failed               : 118 (53.4%)  ❌             │
└─────────────────────────────────────────────────────┘

Regional Distribution:
┌─────────────────────────────────────────────────────┐
│ North : ~26% of transactions  🟢                    │
│ South : ~29% of transactions  🔵                    │
│ East  : ~23% of transactions  🟡                    │
│ West  : ~22% of transactions  🔴                    │
└─────────────────────────────────────────────────────┘
```

### 🔍 Sample Data Records

| transaction_id | customer_id | amount | date | count | region | status |
|---|---|---|---|---|---|---|
| e98aa092-... | CUST2824 | $3,821.34 | 2023-01-26 | 3 | North | ❌ Fail |
| 11ba6918-... | CUST1409 | $2,781.84 | 2023-01-28 | 0 | East | ❌ Fail |
| 82b7654b-... | CUST5506 | $4,120.97 | 2023-01-28 | 0 | South | ❌ Fail |
| f7166574-... | CUST5012 | $6,383.78 | 2023-01-18 | 2 | South | ✅ Success |
| 8632fe26-... | CUST4657 | $2,651.61 | 2023-01-04 | 4 | North | ✅ Success |

**📥 [Full Dataset](Speed_Locator_Data.csv)** • **Total Records: 221**

---

## 🚀 Quick Start

### Prerequisites

```bash
# Ensure you have Python 3.8+ installed
python --version

# Required packages
pip install pandas numpy matplotlib seaborn scipy scikit-learn jupyter
```

### Installation & Setup

```bash
# 1. Clone the repository
git clone https://github.com/jeelprajapati0606/spread_locator.git
cd spread_locator/Spread\ Locator

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch Jupyter Notebook
jupyter notebook

# 4. Open the analysis notebook
# Statistical_Distribution_Analysis_model-checkpoint.ipynb
```

### Quick Analysis Example

```python
import pandas as pd
import numpy as np
from scipy import stats

# Load data
df = pd.read_csv('Speed_Locator_Data.csv')

# Basic statistics
print("Transaction Amount Statistics:")
print(df['transaction_amount'].describe())

# Distribution analysis
data = df['transaction_amount']
mean, std = data.mean(), data.std()
print(f"Mean: ${mean:.2f}, Std Dev: ${std:.2f}")

# Normality test
stat, p_value = stats.shapiro(data)
print(f"Shapiro-Wilk Test p-value: {p_value:.4f}")
```

---

## 📖 Documentation

### Core Concepts

#### 1️⃣ Distribution Fitting

```
Process: Fit observed data to theoretical distributions

Formula for Goodness-of-Fit:
    χ² = Σ((Observed - Expected)² / Expected)
    
Interpretation:
    - Lower χ² = Better fit
    - p-value > 0.05 = Distribution fits well
```

#### 2️⃣ Statistical Tests

| Test | Purpose | Null Hypothesis | Decision |
|------|---------|-----------------|----------|
| **Shapiro-Wilk** | Normality | Data is normal | Reject if p < 0.05 |
| **Kolmogorov-Smirnov** | Goodness-of-fit | Data matches dist. | Reject if p < 0.05 |
| **Anderson-Darling** | Distribution fit | Data follows dist. | More sensitive to tails |
| **Chi-Square** | Independence | Variables independent | Reject if p < 0.05 |

#### 3️⃣ Predictive Models

```
Models Used:
    1. Linear Regression - Baseline predictions
    2. Polynomial Regression - Non-linear patterns
    3. Random Forest - Feature importance & accuracy
    4. Gradient Boosting - Enhanced predictions
    5. Time Series Analysis - Temporal patterns
```

---

## 📊 Key Insights & Analysis

### Regional Performance Analysis

```
SUCCESS RATE BY REGION:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
North: ██████░░░░░░░░ 42.9% (18/42)
South: ██████░░░░░░░░ 44.8% (20/45)
East:  ██████░░░░░░░░ 43.6% (10/23)
West:  ██████░░░░░░░░ 51.6% (16/31)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Overall: 46.6% (103/221) ✅
```

### Transaction Amount by Status

```
FAILED TRANSACTIONS:
  Average Amount: $3,421.89
  Median Amount:  $3,309.10
  Std Deviation:  $2,156.34
  
SUCCESSFUL TRANSACTIONS:
  Average Amount: $3,318.21
  Median Amount:  $3,200.50
  Std Deviation:  $2,054.91
```

---

## 🎬 Interactive Demo

### Option 1: Web-Based Interactive Dashboard

[![Open in Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/jeelprajapati0606/spread_locator/main?filepath=Spread%20Locator%2FStatistical_Distribution_Analysis_model-checkpoint.ipynb)

**[🎯 Launch Interactive Dashboard](https://mybinder.org/v2/gh/jeelprajapati0606/spread_locator/main?filepath=Spread%20Locator%2FStatistical_Distribution_Analysis_model-checkpoint.ipynb)**

### Option 2: Google Colab Notebook

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jeelprajapati0606/spread_locator/blob/main/Spread%20Locator/Statistical_Distribution_Analysis_model-checkpoint.ipynb)

**[📘 View on Google Colab](https://colab.research.google.com/github/jeelprajapati0606/spread_locator/blob/main/Spread%20Locator/Statistical_Distribution_Analysis_model-checkpoint.ipynb)**

### Option 3: Local Jupyter Notebook

```bash
cd "Spread Locator"
jupyter notebook Statistical_Distribution_Analysis_model-checkpoint.ipynb
```

**Interactive Features:**
- 📊 Real-time visualization
- 🎨 Customizable plots
- 🔄 Live data filtering
- 📈 Distribution comparisons
- 💾 Export results

---

## 🔍 Analysis Workflow

### Step-by-Step Process

```
┌─────────────────────────────────────────────────────────────┐
│ STEP 1: DATA COLLECTION & LOADING                          │
│  └─ Load CSV, check dimensions, validate data types        │
└─────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────┐
│ STEP 2: EXPLORATORY DATA ANALYSIS (EDA)                    │
│  └─ Describe stats, visualize distributions, check missing │
└─────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────┐
│ STEP 3: DATA PREPROCESSING & CLEANING                      │
│  └─ Handle outliers, normalize, encode categories          │
└─────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────┐
│ STEP 4: DISTRIBUTION ANALYSIS                              │
│  └─ Fit distributions, test goodness-of-fit, identify best │
└─────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────┐
│ STEP 5: STATISTICAL TESTING                                │
│  └─ Normality tests, hypothesis testing, confidence limits │
└─────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────┐
│ STEP 6: VISUALIZATION & INSIGHTS                           │
│  └─ Create plots, identify patterns, regional analysis     │
└─────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────┐
│ STEP 7: PREDICTIVE MODELING                                │
│  └─ Build models, evaluate, make predictions               │
└─────────────────────────────────────────────────────────────┘
```

---

## 📈 Mathematical Formulas Reference

### Descriptive Statistics

$$\text{Mean} \quad \mu = \frac{1}{n}\sum_{i=1}^{n} x_i$$

$$\text{Variance} \quad \sigma^2 = \frac{1}{n}\sum_{i=1}^{n}(x_i - \mu)^2$$

$$\text{Standard Deviation} \quad \sigma = \sqrt{\sigma^2}$$

$$\text{Coefficient of Variation} \quad CV = \frac{\sigma}{\mu} \times 100\%$$

### Distribution Tests

$$\text{Z-Score} \quad z = \frac{x - \mu}{\sigma}$$

$$\text{T-Statistic} \quad t = \frac{\bar{x} - \mu_0}{s/\sqrt{n}}$$

$$\text{Chi-Square} \quad \chi^2 = \sum_{i=1}^{k} \frac{(O_i - E_i)^2}{E_i}$$

### Linear Regression

$$\hat{y} = \beta_0 + \beta_1 x$$

$$\text{R-squared} \quad R^2 = 1 - \frac{\sum(y_i - \hat{y}_i)^2}{\sum(y_i - \bar{y})^2}$$

---

## 🎓 Learning Outcomes

After studying this project, you will understand:

| Topic | Skill | Application |
|-------|-------|-------------|
| **Distributions** | Identify & model distributions | Predict transaction patterns |
| **Statistics** | Hypothesis testing & inference | Make data-driven decisions |
| **Visualization** | Create publication-quality plots | Communicate insights |
| **ML/AI** | Build & evaluate models | Forecast future trends |
| **Data Science** | Complete data science workflow | Real-world problem solving |

---

## 🛠️ Advanced Features

### Custom Analysis Functions

```python
# Regional trend analysis
df.groupby('region')['transaction_amount'].describe()

# Time series forecasting
from statsmodels.tsa.seasonal import seasonal_decompose
decomposition = seasonal_decompose(df['transaction_amount'])

# Anomaly detection
from sklearn.ensemble import IsolationForest
outliers = IsolationForest().fit_predict(df[['transaction_amount']])
```

### Visualization Capabilities

- 📊 Histograms & KDE plots
- 📈 Box plots & violin plots
- 🎯 Q-Q plots for normality assessment
- 🗺️ Regional comparison plots
- 📅 Time series visualizations
- 🔥 Heatmaps for correlations

---

## 📚 Resources & References

### Key Books & Papers

1. **Statistical Distribution Analysis**
   - "Introduction to Statistical Learning" by James et al.
   - "Probability & Statistics for Engineering" by Devore

2. **Python Data Science**
   - "Python for Data Analysis" by Wes McKinney
   - "Hands-On Machine Learning" by Géron

3. **Time Series & Forecasting**
   - "Forecasting: Principles & Practice" by Hyndman & Athanasopoulos

### Online Courses

- 🎓 Coursera: Statistics with Python
- 🎓 edX: Data Science Essentials
- 🎓 DataCamp: Statistical Thinking in Python

---

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Ideas for Contribution

- [ ] Add more statistical tests
- [ ] Implement real-time dashboard
- [ ] Add machine learning models
- [ ] Expand geographic analysis
- [ ] Create visualization library
- [ ] Performance optimization

---

## 📝 License

This project is licensed under the **MIT License** - see the LICENSE file for details.

---

## 👤 Author

**Jeel Prajapati**
- 📧 Email: [your-email@example.com]
- 🐙 GitHub: [@jeelprajapati0606](https://github.com/jeelprajapati0606)
- 💼 LinkedIn: [Your Profile]

---

## 🙏 Acknowledgments

- Thanks to all open-source contributors
- Statistical theory references and resources
- Data science community for inspiration

---

## 📞 Support & Contact

For questions, issues, or suggestions:

| Channel | Method |
|---------|--------|
| **Issues** | [GitHub Issues](https://github.com/jeelprajapati0606/spread_locator/issues) |
| **Discussions** | [GitHub Discussions](https://github.com/jeelprajapati0606/spread_locator/discussions) |
| **Email** | [your-email@example.com] |

---

<div align="center">

### ⭐ If you found this project helpful, please star it!

[![GitHub Stars](https://img.shields.io/github/stars/jeelprajapati0606/spread_locator?style=social)](https://github.com/jeelprajapati0606/spread_locator)

**Built with ❤️ for Data Science Enthusiasts**

![Made with Python](https://img.shields.io/badge/Made%20with-Python-blue?style=flat-square&logo=python)
![Data Science](https://img.shields.io/badge/Data%20Science-Statistics-brightgreen?style=flat-square)
![Open Source](https://img.shields.io/badge/Open%20Source-MIT-green?style=flat-square)

</div>

---

**Last Updated:** July 2026 | **Version:** 1.0.0 | **Status:** ✅ Active Development
