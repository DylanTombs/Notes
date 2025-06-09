
[[Python]] 



[QuantConnect]

| Feature             | Description                                                                         |
| ------------------- | ----------------------------------------------------------------------------------- |
| **Backtesting**     | Fast, accurate, institutional-grade backtesting                                     |
| **Live Trading**    | Supports brokers like Interactive Brokers, Coinbase, Binance, FXCM, OANDA, and more |
| **Historical Data** | Built-in access to equities, options, futures, forex, crypto, and alternative data  |

[BackTrader]

Core Syntax:

```
import backtrader as bt

class MyStrategy(bt.Strategy):
    params = (('ema_period', 20),)  # Configurable parameters
    
    def __init__(self):
        self.ema = bt.indicators.EMA(period=self.p.ema_period)  # Indicators
        
    def next(self):
        if self.data.close[0] > self.ema[0]:  # Current price > EMA
            self.buy(size=100)  # Go long
        elif self.data.close[0] < self.ema[0]:
            self.sell(size=100)  # Go short

cerebro = bt.Cerebro()  # Engine
cerebro.adddata(bt.feeds.YahooFinanceData(dataname='AAPL', fromdate=datetime(2020,1,1)))
cerebro.addstrategy(MyStrategy)
results = cerebro.run()  # Backtest
cerebro.plot()  # Visualize
```

Indicators:

```
self.sma = bt.indicators.SMA(period=15)
self.rsi = bt.indicators.RSI(period=14)
```

Data Feeds:

```
data = bt.feeds.PandasData(dataname=df)  # Pandas DataFrame
```

Optimisation:

```
cerebro.optstrategy(MyStrategy, ema_period=range(10, 30, 5))  # Param sweep
```

Commission & Sizing:

```
cerebro.broker.setcommission(commission=0.001)  # 0.1% fee
cerebro.addsizer(bt.sizers.PercentSizer, percents=10)  # Risk 10% per trade
```

Useful Snippets:

**Rolling Sharpe Ratio**:

```
from backtrader.analyzers import SharpeRatio
cerebro.addanalyzer(SharpeRatio, _name='sharpe')
```


[yFinance]

```
data = yf.download('AAPL', start='2020-01-01', end='2023-01-01')
```









