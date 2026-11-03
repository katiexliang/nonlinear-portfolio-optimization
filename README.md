# Nonlinear Portfolio Optimization: Risk–Return Analysis

A team research project comparing selected equities associated with the disclosed portfolios of U.S. political figures **Nancy Pelosi** and **John Boozman**, using **2024 historical stock market data** to examine portfolio composition and nonlinear risk–return optimization.

**Project type:** Business Analytics / Financial Analytics · Python · Portfolio Optimization  
**Time period analyzed:** January 2024 – December 2024

## Research objective

Explore how alternative allocations across selected equities might balance expected returns with portfolio risk. The project includes exploratory data analysis, correlation and covariance analysis, constrained optimization, and sensitivity analysis across risk limits.

## Methods and tools

- **Market data retrieval:** `yahooquery` / historical stock prices for selected tickers.
- **Data preparation:** Python, pandas and NumPy; reshaping and imputing historical price series.
- **Exploratory analysis:** descriptive statistics, individual-stock plots, volatility comparisons, time-series charts, and correlation / covariance matrices.
- **Nonlinear portfolio optimization:** Pyomo models with an external IPOPT solver; portfolio allocation experiments under alternative constraints.
- **Visualization:** Matplotlib and Seaborn plots, including efficient-frontier-style risk/return comparisons.

## Files

| File | Description |
| --- | --- |
| `01_Nancy_Pelosi_Analysis.ipynb` | Pelosi-focused EDA and optimization, with saved plots and original analysis. |
| `02_John_Boozman_Analysis.ipynb` | Boozman-focused EDA and optimization, with saved plots and original analysis. |
| `Portfolio_Optimization_Presentation.pdf` | 28-page team presentation with research process, figures and findings. |
| `requirements.txt` | Main Python packages used by the notebook. |

## Key presentation results

The team's presentation reports the following comparisons (see the original slides for details):

| Portfolio | Reported baseline | Reported selected model |
| --- | --- | --- |
| Nancy Pelosi | Risk 100%; return 60% | Risk 5%; return 60% |
| John Boozman | Risk 100%; return 70% | Risk 15%; return 40% |

**Important:** These are the team's *reported model labels/results*, not independently verified annualized investment returns or directly comparable standard portfolio-risk measures. The underlying code should be reviewed before using the output for investment decisions.

## Running the notebook

1. Download or clone this repository.
2. Create a Python environment and install Python dependencies: `pip install -r requirements.txt`.
3. Open `01_Nancy_Pelosi_Analysis.ipynb` or `02_John_Boozman_Analysis.ipynb` with Jupyter or Google Colab. The original large notebook was divided by portfolio to make both files easier to preview on GitHub; all original analytical cells and saved charts are retained, with plot images recompressed.
4. The notebook fetches 2024 market history through Yahoo-related tools and produces CSV files during execution; **a separate raw dataset is not required for the initial fetch**.
5. The optimization sections **require a working IPOPT executable**, and some original notebook cells assume the Google Colab path `/content/ipopt` and use `gdown` to retrieve a solver archive. Review that external binary source and adjust the solver path for your environment before running these sections.

### Reproducibility notes and limitations

- **Notebook outputs are saved results from the original analysis.** Successful re-execution was not verified in preparing this repository.
- The notebook was originally authored for Google Colab, and some cells rely on Colab-specific shell commands. The installation of Python packages alone does not install IPOPT.
- Financial API responses and adjusted-price calculations may differ from the original 2024 snapshot when rerun later.
- Both notebooks write a file called `portfolio_stock_data.csv`. Rename the output or run them in separate folders if you want to retain both generated datasets.
- The objective, constraints, units and interpretation of the risk–return percentages should be checked before treating them as investment performance claims.
- This is a **course research project**, not investment advice or a reconstruction of verified full personal holdings.

## Team and attribution

**Team 10:** Aviral Narang, Dongwook Lee, Flavie Favreaux, and Katie Liang. This is a collaborative academic assignment; the notebook and accompanying presentation reflect team work.

## Data and sources

- Historical market data retrieved via Yahoo-related Python libraries (see the notebook).
- Congressional stock-disclosure information as discussed within the original assignment; the source records and transaction values should be independently confirmed before reuse.

---
*For educational and portfolio demonstration purposes only. Past prices and model estimates do not guarantee future performance.*
