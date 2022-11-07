# EUR/USD Set live candidate - 2022
## New Position Settings
Indicators:
- Medium Average indicator: the goal of this inidicator is a long term main trend filtering. Here are the main parameters:
    - Timeframe: 1 Day
    - Period: 200
- Stochastic indicator: short term indicator to open the position, when in "agreement" with the long term MA above. Main settings:
    - Timeframe: 15 Minutes
    - k-period: 5, d-period: 3

## Grid and hedging settings
- Fixed Grid step: 150 points
- Indicator for grid: MA with hour timeframe, 50 periods - evaluate the benefits of switchint to 25-30
- Lot size:
    - starting lot: 0.01
    - increase: no function, minimum increase of 0.01
- Hedging: enabled from 4th order, MA indicator of 4 hours 
- Time distance between orders: 10 mins

## Risk management settings
- Drowdown reduction (DDR):
    - min orders: 3
    - profit used: 50% (fixed value)
    - multiple orders: yes, 3 orders max
- Piggy bank:
    - Orders # to activate: 10
    - Min loss: 50
    - Profit to use: 50%
    - All pairs: yes
