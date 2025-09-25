## Intro
Started as running in the server on demo account

RUN done on EURUSD from 19/05/2022 to 24/09/2025

## Notes
### Drawdown Reduction
Demo is still using position based, improved with the lot size to improve it:

Position count setting before changing
Steps: 3,7,10,15
Perc: 30,40,60,80

Converted with lots in:
Steps: 0.05,0.15,0.20,0.25,0.5
Perc: 30,40,60,80,100


## Grid
Kept the increasing lot grid:
- start 0.01
- increase of 0.01 every 2 positions
- max grid position size: 0.08
- max number of positions (count is on DB) of 20
- fixed grid step of 500


## Hedging
Changed the hedging, even on BOT code side, in order to have the starting of the hedging not from number of positions, but from Quantiy.

### Main settings
- start from 0.05 opposite lots
- start also if opposite take profit is more than 1500 points away from current price
- cover 80% of the opposite positions
- spread opposite positions across max 1200 points price range
- add a max of 20 hedging positions (never seen hedging limited by this, to check)

### Code changes
- sync all the logic to define if hedging is enabled in a single point
- added the hedging enable also if the take profit is too fara away