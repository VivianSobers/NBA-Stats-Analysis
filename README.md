# NBA-Stats-Analysis

## Overview

This project scrapes NBA 2024 season player statistics from [Basketball Reference](https://www.basketball-reference.com/leagues/NBA_2024_totals.html), cleans and preprocesses the data, performs descriptive statistical analysis, and visualizes key patterns across player positions and performance metrics.

Done as part of **UE24MA242A — Mathematics for Computer Science Engineers** at PES University (Aug–Dec 2025).

---

### 1. Web Scraping
- Fetches the NBA 2024 totals table from Basketball Reference using `urllib` and `BeautifulSoup`
- Extracts player stats: Position, FG%, FG3%, FG2%, FT%, Offensive Rebounds, Defensive Rebounds, Assists, Blocks, Steals, Points
- Stores cleaned data into `nba_player_stats.csv`

### 2. Data Preprocessing
- Detects and drops rows with missing values
- Fills missing `FG3%` and `FT%` with column mode
- Converts all stat columns to numeric types using `pd.to_numeric`
- Removes header repeat rows injected by the source HTML table

### 3. Descriptive Statistics
- Mean points, assists, rebounds grouped by position
- Median FG3% and steals per position
- Standard deviation of FG3%, steals, and blocks
- Variance of blocks
- Full `describe()` summary across all numeric columns

### 4. Visualizations

| Plot | Description |
|------|-------------|
| Bar chart | Average points per position |
| Grouped bar chart | Average FG3%, FG2%, FT% per position |
| Boxplot | Assists distribution per position |
| Boxplot | Offensive rebounds per position |
| Boxplot | Defensive rebounds per position |
| Scatter plot | Assists vs Steals |
| Scatter plot | Offensive vs Defensive rebounds |
| Scatter plot | 2-pointer % vs 3-pointer % |
| Histogram | Distribution of FG3% |
| Histogram | Distribution of FT% |
| Histogram | Distribution of FG% |
| Pair plot | Pts, FG%, FG3%, FT% relationships |
| Heatmap | Correlation matrix of all numeric stats |

---

## How to Run

### 1. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn beautifulsoup4
```

### 2. Open the notebook

```bash
jupyter notebook NBA.ipynb
```

### 3. Run all cells
The notebook will scrape, clean, analyse, and plot everything end to end. The CSV will be saved as `nba_player_stats.csv` in the same directory.

---

## Project Structure

```
nba-stats-analysis/
├── NBA.ipynb               # Main notebook — scraping, cleaning, analysis, plots
├── nba_player_stats.csv    # Generated CSV of cleaned player stats
└── README.md
```

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| `BeautifulSoup4` | HTML parsing and web scraping |
| `urllib` | Fetching the web page |
| `Pandas` | Data manipulation and cleaning |
| `NumPy` | Numerical operations |
| `Matplotlib` | Base plotting |
| `Seaborn` | Statistical visualizations |

---

## Data Source

**Basketball Reference — NBA 2024 Player Totals**
`https://www.basketball-reference.com/leagues/NBA_2024_totals.html`

---

## Author

**Vivian Sobers E** — [github.com/VivianSobers](https://github.com/VivianSobers)
