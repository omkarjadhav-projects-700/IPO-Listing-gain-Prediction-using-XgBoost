# 🚀 IPO Listing Gain Prediction for Indian Markets (Ongoing Project)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.2%2B-orange?logo=scikit-learn)
![XGBoost](https://img.shields.io/badge/XGBoost-1.7%2B-green?logo=xgboost)
![Pandas](https://img.shields.io/badge/Pandas-1.5%2B-darkblue?logo=pandas)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

## 📖 Overview

This project is a comprehensive end-to-end machine learning pipeline designed to predict the short-term **listing gain** of Initial Public Offerings (IPOs) on Indian stock exchanges (NSE/BSE). The model leverages a rich dataset of over 40 features—scraped from financial platforms like Chittorgarh, Moneycontrol, and NSE—encompassing subscription figures, financial ratios, promoter holding patterns, and issue structure to forecast market performance.

Accurately predicting IPO success is a classic challenge in quantitative finance. This solution demonstrates the ability to process complex, multi-source financial data and build a robust predictive model, showcasing strong skills in data engineering and machine learning.

## 🎯 Motivation

The Indian primary market has seen record-breaking participation in recent years. For retail investors, identifying IPOs with high potential listing gains is highly lucrative but complex. This project aims to:
*   Demystify the factors driving IPO underpricing in the Indian context.
*   Provide a data-driven tool to estimate potential short-term returns.
*   Serve as an advanced portfolio piece demonstrating expertise in ML, web scraping, and financial analysis.

## 🗃️ Dataset & Features

The dataset is manually curated by scraping and consolidating information from multiple reliable sources to ensure robustness. The feature set is extensive and can be categorized as follows:

*   **Issue Details:** `issue_type`, `sale_type`, `fresh_issue_shares`, `offer_for_sale`, `price_band`, `lot_size`.
*   **Subscription Data:** Subscription multiples for `QIB`, `NII`, `Retail`, and `Employee` categories, including shares offered vs. bid for.
*   **Financial Metrics:** Pre and Post-IPO `EPS`, `P/E Ratio`, `ROE(%)`, `ROCE(%)`, `Debt/Equity`, `PAT Margin(%)`, `Price to Book Value`.
*   **Promoter Holding:** `Promoter_shareholding_pre_issue(%)` and `Promoter_shareholding_post_issue(%)`.
*   **Target Variable:** `listing_gain` - The percentage gain or loss on the listing day compared to the issue price.

> **Note:** The provided Excel file (`data_creation.xlsx`) showcases the schema and a sample data point for the 2024 IPO of Afcons Infrastructure Ltd.

## ⚙️ Tech Stack & Methodology

### 1. Data Acquisition & Engineering
*   **Tools:** `Python`, `Pandas`, `NumPy`, `Requests`, `BeautifulSoup`/`Selenium`
*   **Process:** Custom web scrapers were built to extract structured data from Chittorgarh, Moneycontrol, and NSE websites. The data was cleaned, normalized, and merged into a unified dataset.

### 2. Feature Engineering & Preprocessing
*   Handled missing values and outliers specific to financial data.
*   Engineered new features that capture the relative demand (e.g., subscription ratios).
*   Performed standardization/normalization of numerical features.

### 3. Machine Learning Modeling
*   **Algorithm:** **XGBoost Regressor** (Extreme Gradient Boosting) was chosen for its high performance on tabular data, ability to handle non-linear relationships, and built-in feature importance.
*   **Training:** The model was trained using a supervised learning approach to predict the continuous `listing_gain` value.
*   **Evaluation:** Model performance is evaluated using:
    *   **Mean Absolute Error (MAE)**
    *   **Root Mean Squared Error (RMSE)**
    *   **R-squared (R²) Score**

### 4. Tools & Libraries
*   **Language:** Python
*   **Libraries:** Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn, Requests, BeautifulSoup4.
*   **Version Control:** Git, GitHub


## 🚦 Getting Started

### Prerequisites
*   Python 3.8+
*   pip

## 📖 References

* https://www.analyticsvidhya.com/blog/2022/12/ultimate-guide-to-boosting-algorithms/
* https://www.analyticsvidhya.com/blog/2018/09/an-end-to-end-guide-to-understand-the-math-behind-xgboost/
* https://www.analyticsvidhya.com/blog/2016/03/complete-guide-parameter-tuning-xgboost-with-codes-python/

## 👨‍💻 Developer

**Omkar Jadhav**
*   LinkedIn: https://www.linkedin.com/in/omkar-jadhav-637807278/
*   Email: omkarjadhav3540@gmail.com

## 📜 License

This project is licensed under the MIT License.

## 🙏 Acknowledgments

*   Data is to be sourced from [Chittorgarh](https://www.chittorgarh.com/), [Moneycontrol](https://www.moneycontrol.com/), and the [NSE](https://www.nseindia.com/).
*   Inspired by research on IPO underpricing and market efficiency.

---

**⭐ Star this repo if you found it interesting!**
