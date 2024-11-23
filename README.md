---

# Stock Price Modeling Using Monte Carlo Simulations

This repository contains the implementation of our course project on stock price modeling, which compares Monte Carlo simulations with traditional and modern forecasting methods.

## **Overview**

Stock prices are influenced by numerous dynamic factors, making their prediction a challenging problem. We explored and compared various methodologies:

1. **ARIMA:** For short-term linear dependencies.
2. **Markov Chains:** For probabilistic transitions between discrete states.
3. **LSTM:** For capturing long- and short-term dependencies in time series.
4. **Monte Carlo Simulations:** Using **Geometric Brownian Motion (GBM)** and **Jump Diffusion Models (GBM-JD)** for modeling uncertainty and volatility.

## **Dataset**

We used stock price data for Apple (AAPL) and Google (GOOG) obtained from [Yahoo Finance](https://finance.yahoo.com).  
- **Training period:** 2015–2020  
- **Testing period:** 2020–2021

## **Key Results**

| **Model**    | **MSE (AAPL)** | **MSE (GOOG)** | **Inference Time (sec)** |
|--------------|----------------|----------------|--------------------------|
| ARIMA        | 1310.78        | 1420.34        | 1.20                    |
| Markov       | 187.09         | 210.12         | 7.80                    |
| LSTM (Large) | 61.40          | 70.12          | 1290.00                 |
| GBM          | 150.66         | 160.78         | 557.40                  |
| GBM-JD       | 125.32         | 130.45         | 587.20                  |

LSTM models achieved the best accuracy but required significant computational resources. Monte Carlo methods, particularly Jump Diffusion, offered a good balance of accuracy and efficiency.

## **Usage**

### **Dependencies**
- Python 3.8+
- Libraries: `numpy`, `pandas`, `matplotlib`, `scikit-learn`, `tensorflow`, `statsmodels`, `yfinance`

Install dependencies using:
```bash
pip install -r requirements.txt
```

### **Running the Code**
1. Clone the repository:
   ```bash
   git clone https://github.com/prabhas2002/Stock_prediction_using_Monte_Carlo_simulations.git
   ```
2. Navigate to the directory:
   ```bash
   cd Stock_prediction_using_Monte_Carlo_simulations
   ```
3. Run simulations:
   ```bash
   python run_simulations.py
   ```
4. Visualize results:
   ```bash
   python visualize_results.py
   ```

## **Future Work**

Future work will focus on:
- Incorporating advanced Monte Carlo methods like Stochastic Volatility Models.
- Experimenting with hybrid models combining simulation and deep learning techniques.

---

Let me know if you'd like any modifications!
