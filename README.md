## Overview
This project examines the 12-month closing price trends of five biotechnology companies (SPRC, ONCY, XBIT, NVCR, and PPBT) involved in pancreatic cancer therapeutics. It then compares their daily returns variance to the Nasdaq Biotechnology Index (NBI), constructs a custom index of the five stocks, analyzes peaks and troughs, and finally uses Meta’s Prophet to forecast the custom index performance over the next 90 days.

## Key Steps
1. **Data Collection:**  
   - Fetches daily historical data (last 12 months) for each stock and for the NBI using `yfinance`.
   - Computes the daily closing prices and daily returns.

2. **Variance Comparison:**  
   - Calculates daily return variances for each stock.
   - Compares them with the NBI’s variance to see which stock’s variance is most similar.

3. **Custom Index Construction:**  
   - Normalizes each of the five stocks to a starting value of 100, then averages them to form a single, equal-weighted custom index.
   - Plots and compares this custom index against the NBI over the same period.

4. **Peak & Trough Analysis:**  
   - Identifies peaks and troughs in both the custom index and the NBI using `scipy.signal.find_peaks`.
   - Plots these peaks/troughs for visual comparison.

5. **Forecasting with Prophet:**  
   - Uses Meta’s Prophet to forecast the custom index 90 days into the future (1) without regressors and then (2) using the NBI as an external regressor.

## Requirements
- Python 3.x
- Packages:
  - `yfinance`
  - `matplotlib`
  - `pandas`
  - `numpy`
  - `scipy`
  - `prophet` (formerly `fbprophet`)

## How to Run
1. **Clone or download** the repository containing this single `.py` or `.ipynb` file.  
2. **Install the required packages** (e.g., via `pip install -r requirements.txt` or manually with `pip install yfinance matplotlib pandas numpy scipy prophet`).  
3. **Execute the code** in a Jupyter Notebook, Google Colab, or any Python 3 environment.  
4. **Follow the sequential outputs** for:
   - Variance analysis
   - Index comparison
   - Peak/trough plots
   - Prophet forecast graphs

## Notes
- This analysis is for educational and illustrative purposes only; it does not constitute financial advice.  
- Data availability depends on `yfinance` and may shift over time.  

## License
This project is provided under the [MIT License](https://opensource.org/licenses/MIT).

## Contact
For questions or suggestions, please open an issue in this repository or reach out via LinkedIn/GitHub.  
