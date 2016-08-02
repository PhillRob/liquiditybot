# Goal
* Make money off volatility
* Assumption - Long term trend of bitcoin will be up
  * If this is not the case, then this will not work

# Algorithm
* Place Buys/Sells at specified intervals (ever EUR 1 for example)
* Start by taking EUR X and placing an equal buy amount (Y BTC) below the current market price at each interval
* If the price goes lower then it will trigger a buy for that order
  * Immediately place a sell order for that bitcoin at EUR 1 higher than the buy price was triggered
    * If a sell order is filled, immediately place a buy order at EUR 1 lower than the sell price was triggered

Reset: If the price goes EUR 10 higher than the highest buy price (and no btc is owned) then reset and create all new buy orders below the current price

If the price goes below all open orders then there is nothing that can be done and we must wait for the price to come back up.

# Docs: 
* https://docs.exchange.coinbase.com/?javascript#orders
* https://www.gdax.com/settings/api

# Install
* get npm packages
```
  $ git clone https://github.com/pooleja/liquiditybot
  $ npm install winston
  $ npm install coinbase-exchange
  $ npm install async
  $ npm install mongodb
  $ npm install winston
  $ npm install gdax
```
