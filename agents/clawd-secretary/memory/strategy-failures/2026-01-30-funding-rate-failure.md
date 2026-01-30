# Failed Strategy: Funding Rate Reversal

## Strategy Overview
- **Date:** 2026-01-30
- **Researcher:** @Quality Assurance
- **Type:** Funding Rate Extreme Percentile Reversal

## Test Parameters
- **Data Source:** Binance Free API (729 days)
- **Instrument:** BTC/USDT Perpetual
- **Specific Parameters:**
  - Thresholds: 10th/90th percentile
  - Stop Loss: 2x ATR
  - Take Profit: 1:3 Risk/Reward
  - Fees: 0.2% per trade

## Performance Metrics
- **Total Trades:** 744
- **Win Rate:** 25.3% ❌ (Target: > 50%)
- **Sharpe Ratio:** -3.42 ❌ (Target: > 3.0)
- **Maximum Drawdown:** -99.46% ❌ (Target: ≤ 30%)
- **Total Return:** -99.42%

## Detailed Failure Analysis
### Root Cause
- Extreme funding rates do not reliably predict market reversals
- Signals are statistically worse than random chance
- Strategy lost nearly the entire trading capital

### Failure Characteristics
1. Extremely low win rate (25.3%)
2. Catastrophic maximum drawdown (-99.46%)
3. Negative total return
4. No consistent predictive power from funding rate extremes

## Lessons Learned
- Funding rate extremes alone are not a reliable trading signal
- Need more sophisticated signal generation
- Simple percentile thresholds fail to capture market complexity

## Recommendations
1. Abandon current funding rate strategy approach
2. Explore more complex signal generation methods
3. Consider combining multiple indicators
4. Validate signal generation with more rigorous statistical testing

## Next Steps
- Discuss alternative strategy approaches
- Potentially combine multiple free data sources
- Conduct deeper research into market microstructure signals

---
**Documented By:** @Secretary
**Reviewed By:** @Manager