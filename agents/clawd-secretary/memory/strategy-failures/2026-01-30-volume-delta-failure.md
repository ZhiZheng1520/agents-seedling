# Failed Strategy: Volume Delta Divergence

## Strategy Overview
- **Date:** 2026-01-30
- **Researcher:** @Developer2
- **Type:** Volume Flow Divergence

## Test Parameters
- **Data Source:** OHLCV Free Candle Data
- **Instrument:** BTC/USDT Perpetual
- **Timeframe:** 15-minute bars
- **Specific Parameters:**
  - Delta window: 20 bars
  - Divergence threshold: 0.2%
  - Volume filter: 1.5x average
  - Stop Loss: 2.0x ATR
  - Take Profit: 1:3 Risk/Reward

## Performance Metrics
- **Sharpe Ratio:** -2.14 ❌ (Target: > 3.0)
- **Maximum Drawdown:** -40.01% ❌ (Target: < 30%)
- **Win Rate:** 40% ❌ (Target: > 50%)
- **Total Trades:** 85

## Detailed Failure Analysis
### Root Cause
- OHLCV candle approximation fails to capture true order flow
- Winning vs losing trades have statistically indistinguishable delta values
  - Bullish divergence wins: -0.126 delta
  - Bullish divergence losses: -0.135 delta

### Specific Failure Modes
1. 54% of trades hit stop loss
2. 0% of trades reached 1:3 take profit target
3. Extreme performance in certain months (e.g., April 2025: 13.3% win rate)
4. Actual Risk/Reward: 1:1.13 vs target 1:3.0

## Key Limitations
- Requires paid trade-by-trade data to work properly
- Free OHLCV data creates false divergence signals
- Candle direction is an inadequate proxy for order flow

## Recommendations
1. Avoid using OHLCV candle direction as volume proxy
2. Seek alternative free data sources
3. Consider pivot to funding rate strategy

## Next Steps
- Pivot to funding rate strategy
- Document lessons learned to prevent similar approaches

---
**Documented By:** @Secretary
**Reviewed By:** @Manager