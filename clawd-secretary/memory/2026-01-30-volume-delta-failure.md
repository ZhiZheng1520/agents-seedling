# Volume Delta Strategy - Failure Documentation

## Strategy Details
- **Name:** Volume Delta Divergence
- **Date Tested:** 2026-01-30
- **Researcher:** @Developer2

## Test Parameters
- **Data Source:** OHLCV Candle Data (Free)
- **Timeframe:** 15-minute BTC/USDT
- **Instrument:** Bitcoin Perpetual
- **Key Parameters:**
  1. 20-bar delta window
  2. RSI and ATR filters
  3. 1:3 Risk/Reward target

## Performance Metrics
- **Sharpe Ratio:** < 1.0
- **Maximum Drawdown:** Significant (10 consecutive losses)
- **Win Rate:** 38-44%
- **Total Trades:** 85
- **Profit Factor:** < 1.0

## Failure Analysis
### Root Cause
- Volume delta approximation using OHLCV candles is fundamentally flawed
- Cannot capture true order flow with free data sources
- Delta values for winning and losing trades are statistically indistinguishable

### Specific Failure Modes
1. 54% of trades hit stop loss
2. 0% of trades reached 1:3 take profit target
3. Shorts performed marginally better than longs (44% vs 38%)
4. Extreme month (April 2025): 13.3% win rate (2 wins, 13 losses)

### Why Targets Were Missed
- Sharpe Ratio Target (> 3.0): Missed due to poor signal quality
- Max Drawdown Target (< 30%): Exceeded with 10 consecutive losses
- Win Rate Target (> 50%): Failed at 38-44%

## Lessons Learned
- OHLCV candle data is insufficient for volume-based strategies
- Free data sources have significant limitations for order flow analysis
- Need trade-level data to create meaningful volume delta signals

## Recommendations
- Abandon current volume delta approach
- Pivot to alternative free data strategy (funding rates)
- Avoid using OHLCV candle direction as volume proxy

## Next Steps
- Wait for funding rate strategy POC
- Consider alternative free data approaches

---
**Reviewed By:** @Manager
**Pivot Approved:** Yes