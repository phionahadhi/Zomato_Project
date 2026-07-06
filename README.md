# Zomato Exploratory Data Analysis

## Project Overview
This project performs an Exploratory Data Analysis (EDA) on the Zomato dataset to uncover insights about restaurant ratings, cuisines, online delivery availability, and geographic distribution of restaurants across different countries.

---

## Dataset
- **Source:** [Zomato Dataset - Kaggle](https://www.kaggle.com/datasets/shrutimehta/zomato-restaurants-data)
- **Files Used:**
  - `zomato.csv` — Main restaurant dataset
  - `Country-Code.xlsx` — Country code lookup table
- **Total Features:** 21 columns after merging

---

## Libraries Used
```
pandas
numpy
matplotlib
seaborn
openpyxl
```

---

## Steps Performed

### 1. Data Loading
- Loaded `zomato.csv` with `latin-1` encoding to handle special characters
- Loaded `Country-Code.xlsx` using `openpyxl`
- Merged both datasets on `Country Code` to get country names

### 2. Missing Value Analysis
- Identified missing values using `isnull().sum()`
- Visualized missing values using a heatmap

### 3. Exploratory Data Analysis

#### Ratings Analysis
- Grouped restaurants by `Aggregate rating`, `Rating color`, and `Rating text`
- Visualized rating distribution using bar plots
- Identified rating color coding:

| Rating Range | Color | Text |
|-------------|-------|------|
| 4.5 – 4.9 | Dark Green | Excellent |
| 4.0 – 4.4 | Green | Very Good |
| 3.5 – 3.9 | Light Green | Good |
| 3.0 – 3.4 | Yellow | Average |
| 2.5 – 2.9 | Orange | Poor |
| 0 | White/Blue | Not Rated |

#### Country Analysis
- Analyzed restaurant distribution across countries using a pie chart
- Identified countries with the most zero ratings

#### Online Delivery Analysis
- Identified which countries offer online delivery
- Compared online delivery availability across countries

#### City Distribution
- Visualized top 5 cities by number of restaurants using a pie chart

#### Cuisine Analysis
- Identified the top 10 most popular cuisines on Zomato

---

## Key Findings

1. **Zomato is India-dominated** — the vast majority of records and transactions are from India, followed by the United States and United Kingdom
2. **High unrated count** — a significant number of restaurants have a 0 rating (not rated), mostly from Indian customers
3. **Maximum ratings fall between 2.5 – 3.4** — suggesting most restaurants are rated Average
4. **Online delivery is limited** — only available in India and UAE; in India most places accept online delivery while others don't
5. **Currency varies by country** — each country uses its own local currency on the platform

---

## How to Run

1. Clone the repository:
```bash
git clone https://github.com/phionahadhi/BlackFriday-Analysis.git
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Open the notebook in VS Code or Jupyter:
```bash
jupyter notebook EDA_and_feature_Engineering.ipynb
```

4. Run all cells from top to bottom

---

## Project Structure
```
├── zomato.csv                          # Main dataset
├── Country-Code.xlsx                   # Country code lookup
├── EDA_and_feature_Engineering.ipynb  # Main analysis notebook
├── requirements.txt                    # Dependencies
└── README.md                           # Project report
```
