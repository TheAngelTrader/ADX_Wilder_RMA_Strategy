<div align="center">

# ADX WILDER RMA STRATEGY

</div>

A comprehensive trading signal system that combines multiple technical indicators to identify high-probability CALL and PUT opportunities. The system filters out weak market conditions by requiring alignment across trend, volatility, directional movement, and momentum indicators.

---
## 📌 Indicators Used
| Indicator | Period | Purpose |
|-----------|--------|---------|
| Moving Average (MA) | 50 | Primary trend direction |
| Hull Moving Average (HMA) | 15 | Short-term trend acceleration |
| ADX Wilder | 14 | Trend strength filter |
| +DI / -DI | 14 | Directional dominance |
| Stochastic | 5,3,3 | Momentum & overbought/oversold levels |

---

## 📈 CALL (BUY) Signal Logic

A CALL signal is generated only when **ALL** conditions are met:
```
✅ Open > MA(50)           → Price above long-term trend
✅ Open > HMA(15)          → Price above short-term acceleration
✅ ADX Main > 25           → Strong trend present
✅ +DI > ADX Main          → Bullish directional pressure
✅ Stoch Main > Stoch Signal → Bullish momentum confirmed
✅ Stoch Main < 80         → Not yet overbought
```

**Result:** Return `1` (CALL Signal)

---

## 📉 PUT (SELL) Signal Logic

A PUT signal is generated only when **ALL** conditions are met:
```
✅ Open < MA(50)           → Price below long-term trend
✅ Open < HMA(15)          → Price below short-term acceleration
✅ ADX Main > 25           → Strong trend present
✅ -DI > ADX Main          → Bearish directional pressure
✅ Stoch Main < Stoch Signal → Bearish momentum confirmed
✅ Stoch Main > 20         → Not yet oversold
```

**Result:** Return `-1` (PUT Signal)

---

## 📊 Backtesting Results

**Tested on:** EUR/USD 1-Minute Chart  
**Total Trades:** 2,238  
**Win Rate:** 50%  
**Maximum Losing Streak:** 9 consecutive losses

### 📉 Loss Streak Distribution

| Streak Length | Frequency | Percentage |
|---------------|-----------|------------|
| 1 Loss | 324 | 54.55% |
| 2 Losses | 132 | 22.22% |
| 3 Losses | 84 | 14.14% |
| 4 Losses | 24 | 4.04% |
| 5 Losses | 12 | 2.02% |
| 6 Losses | 10 | 1.68% |
| 7 Losses | 7 | 1.18% |
| 9 Losses | 1 | 0.17% |

---

## 🎯 Key Observations

- **Win Rate:** The 50% win rate indicates the system requires proper money management and risk-reward optimization
- **Streak Analysis:** 54.55% of losing streaks are single losses, showing good recovery potential
- **Maximum Drawdown:** Only 9 consecutive losses (0.17% probability) indicates relatively controlled risk
- **Trend Filtering:** The multi-indicator approach effectively filters low-quality setups

---
### 📉 Back Test
![EURUSD Backtest](EURUSD_BackTest.png)




---


