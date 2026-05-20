# 🌍 World Happiness Report 2019 — Exploratory Data Analysis

A data analysis project exploring the relationships between national happiness scores and socioeconomic indicators across 156 countries using the [World Happiness Report 2019 dataset](https://www.kaggle.com/datasets/unsdsn/world-happiness).

---

## 📌 Project Overview

This project investigates what factors most strongly correlate with national happiness, with a particular focus on GDP per capita as a predictor. Beyond standard visualization, the analysis includes **custom outlier detection logic** to surface countries that behave unexpectedly relative to global averages — countries that are either happier than their wealth suggests, or wealthier than their happiness reflects.

---

## 🔍 Key Questions Explored

- Which countries rank highest and lowest in happiness globally?
- How strongly does GDP per capita correlate with happiness score?
- Which countries are outliers — and what makes them statistically interesting?

---

## 📊 Visualizations Produced

| Visualization | Description |
|---|---|
| Top 20 Happiest Countries | Horizontal bar chart with gradient palette |
| Bottom 20 Least Happy Countries | Comparative bar chart |
| GDP vs Happiness (Scatter) | Size and hue-encoded scatter plot |
| GDP vs Happiness (Regression) | Trend line overlay with `regplot` |
| Outlier-Labeled Scatter | Custom threshold-based labeling with non-overlapping annotations |

---

## 🧠 Technical Highlights

- **Custom outlier detection**: Countries were flagged and labeled using mean-threshold logic across two dimensions (GDP and happiness score), identifying statistically interesting edge cases rather than plotting all 156 labels
- **Non-overlapping annotations**: Used the `adjustText` library to automatically reposition country labels with leader lines — a common challenge in dense scatter plots
- **Column normalization**: Renamed all dataset columns for consistency and programmatic ease before analysis

---

## 🛠️ Tech Stack

- **Python 3.13**
- **pandas** — data loading, cleaning, column normalization
- **matplotlib** — core plotting and figure configuration
- **seaborn** — statistical visualizations (barplot, scatterplot, regplot)
- **plotly.express** — interactive visualization support
- **adjustText** — automatic label placement for annotated scatter plots

---

## 📁 Dataset

- **Source**: [Kaggle — World Happiness Report](https://www.kaggle.com/datasets/unsdsn/world-happiness)
- **Year**: 2019
- **Size**: 156 rows × 9 columns
- **Features**: Overall rank, country, happiness score, GDP per capita, social support, healthy life expectancy, freedom, generosity, perceptions of corruption

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/yasirshah-csds/world-happiness-eda.git
cd world-happiness-eda

# Install dependencies
pip install pandas matplotlib seaborn plotly adjustText

# Launch the notebook
jupyter notebook happiness.ipynb
```

---

## 📈 Sample Insight

Countries with high GDP but below-average happiness scores — such as certain Gulf states — suggest that wealth alone is insufficient for national well-being. Conversely, several Latin American countries score significantly above their GDP would predict, pointing to the influence of social support and freedom metrics.

---

## 👤 Author

**Yasir Shah** — Data Science Student, University of Michigan–Dearborn  
🔗 [GitHub](https://github.com/yasirshah-csds)
