

---

## 🧠 Overview of the Simulator
- **Goal**: Simulate real financial markets. You’ll rotate through roles (Market Maker, Sales Trader, Buy-Side Analyst).
- **Duration**: 2 hours (approx. 3 rounds, 40 minutes each).
- **Skills Tested**: 
  - Communication  
  - Pricing & quoting
  - Risk management  
  - Market analysis  
  - Client handling

---

## 💼 Roles & Responsibilities

### 🟡 Market Maker
- **Key Task**: Provide bid/ask quotes.
- **Focus**:
  - Narrow spreads for high liquidity.
  - Hedge risk using correlated assets.
  - Use **Order Book**, **P&L**, and **Inventory Monitor** actively.
- **Tips**:
  - Avoid large inventory imbalances.
  - Price assets with news-driven expectations.
  - Adjust pricing quickly to market sentiment.

### 🔵 Sales Trader
- **Key Task**: Manage client relationships & execute trades.
- **Focus**:
  - Communicate clearly with clients.
  - Quote competitively while protecting MM's risk.
  - Upsell when appropriate.
- **Tips**:
  - Track each client’s risk appetite.
  - Bridge MM ↔ Client: Translate needs into good quotes.
  - Think fast: don’t leave clients waiting.

### 🟢 Buy-Side Analyst (Asset Manager)
- **Key Task**: Analyze news & place trades.
- **Focus**:
  - Read breaking news fast.
  - Adjust portfolio for alpha.
  - Exploit pricing inefficiencies.
- **Tips**:
  - Be aggressive early if confident.
  - Diversify trades across assets.
  - Focus on long-term vs. short-term gain.

---

## 📊 Key Concepts & Terms

- **Bid/Ask Spread**: Difference between buying and selling price.
- **Liquidity**: Ease of buying/selling without affecting price.
- **Volatility**: Price fluctuation frequency.
- **Correlation**: How assets move relative to each other.
- **News Shock**: Key driver of asset value change.

---

## 🧩 Strategies

### 📈 General
- Pay attention to **breaking news**—acts as a signal.
- Watch **price trends** + **volume surges**.
- Don’t get stuck watching one screen—rotate tabs actively.

### 🟡 Market Maker
- Hedge positions—don’t be net long/short in one asset.
- Adjust spread depending on market sentiment.
- Use **cross-asset arbitrage** if correlation breaks.

### 🔵 Sales Trader
- Build rapport: "I’d recommend this because..."
- Protect MM while keeping client happy.
- Stay cool under pressure—prioritize bigger clients.

### 🟢 Buy-Side Analyst
- Use news to front-run market moves.
- Spread capital across 2–3 strong convictions.
- Be early—first-movers win.

---

## 🛠️ Tools You’ll Use

- **Trader Terminal**: Live prices, charts, portfolio.
- **News Feed**: Rapid updates — **read headlines FAST**.
- **Chat**: Interact with clients/MMs — keep it short + sharp.
- **Risk Dashboard**: Monitor P&L, VaR, exposure.

---

## 🟨 How to Think Like a Trader

- **Everything is about Supply & Demand**  
  → News changes how people feel about value → prices move.  
  → If many people want to buy: price ↑. If they panic and sell: price ↓.

- **You Don’t Need to Know Everything**  
  → Your job is to **react to information quickly** and **manage risk**.  
  → Focus on **probabilities**, not predictions.

- **Asset Prices Reflect Expectations**  
  → Prices move when *new info* breaks existing expectations.

---

## 🗞️ How to Interpret News in the Simulator

- **Positive News**:
  - Economic growth, good earnings → prices likely to go UP
  - For commodities: supply shortage → price ↑

- **Negative News**:
  - Interest rate hikes, inflation concerns, scandals → price ↓

- **Correlated Assets**:
  - If news says “Gold is up due to war concerns,” **expect oil to move too**.
  - Look for patterns like “risk-on” (stocks up, bonds down) or “risk-off” (stocks down, gold up).

---

## 🧮 Buy/Sell Decision Checklist

- 🔎 **Has news changed the value?**
- 📊 **Is the price reflecting that change yet?**
- 🕒 **Am I early enough to profit, or is it already priced in?**
- 📈 **Trend confirmation**: Is price moving in that direction?
- ⚖️ **What’s my risk if I’m wrong?**

---

## 🧷 Risk Management Tips

- Never go “all in” — keep buffer cash.
- Diversify if unsure — e.g., 2 long, 1 short.
- Don’t try to "win back" losses quickly — that’s gambling.
- Use “stop loss” logic in your head: cut bad trades early.

---

## 🧠 Mental Models

- **Second-Order Thinking**:  
  “If this news is good for oil, what will it do to airline stocks?”

- **Mean Reversion**:  
  Assets often return to a "fair value" after hype/panic.

- **Momentum**:  
  If price is moving fast after news, others might join → temporary trend.

---

# 📊 Core Finance Concepts for AmplifyME Simulation

---

## 🏛️ 1. Market Structure (How Markets Work)

- **Two-Sided Market**: Always a *bid* (buy) and *ask* (sell).
  - 💡 *You can make money by being between them* (Market Maker role).
- **Liquidity**: How easily you can buy/sell without moving price.
- **Market Participants**:
  - **Buy-Side**: Funds, analysts, clients (take positions)
  - **Sell-Side**: Brokers, traders, market makers (provide liquidity)

---

## 📉 2. Order Types

- **Market Order**: Executes immediately at best available price.
  - ✔ Fast but risk of bad fill.
- **Limit Order**: Sets a price; executes only if matched.
  - ✔ Control over price, ❌ May not execute.
- **Stop Loss**: Triggers a sell when price hits certain point.
  - 🛑 Helps manage downside.

---

## 📈 3. Asset Classes You Might Trade

### 🟡 Equities (Stocks)
- Driven by:
  - Earnings reports
  - Economic growth
  - Investor sentiment
- React to **news about company performance, interest rates, inflation**

### ⚪ Commodities (Oil, Gold)
- Driven by:
  - Supply & demand shocks
  - Geopolitical tension (gold ↑ during war)
  - Inflation hedge

### 🔵 Bonds
- Driven by:
  - Interest rates (inverse relationship)
  - Credit risk
  - Inflation expectations

---

## 💵 4. Interest Rates & Central Banks

- **If rates go up**:
  - Bonds fall (fixed payments worth less)
  - Stocks may fall (higher discount rate)
  - Currencies strengthen

- **If rates go down**:
  - Bonds rise
  - Stocks may rise
  - Currencies weaken

- **Central Banks (e.g. Fed)** control:
  - Interest rates
  - Inflation targets
  - Liquidity injections

---

## 🧠 5. Economic Indicators (Common in AmplifyME News)

| Indicator | What It Means | Reaction |
|----------|----------------|----------|
| GDP Growth | Strong economy | Equities ↑ |
| Inflation (CPI) | Prices rising | Bonds ↓, Rates ↑ |
| Unemployment | Weak job market | Equities ↓ |
| PMI | Business confidence | High = Equities ↑ |
| Interest Rate Hike | Cost of capital ↑ | Equities ↓, Bonds ↓ |
| Fed Dovish Talk | Easier policy | Equities ↑, Bonds ↑ |

---

## 📊 6. Quick Valuation Terms

- **Price = Present Value of Expected Cash Flows**
- **Discount Rate**: Higher = lower price (inverse relation)
- **Yield Curve**:
  - Normal: Longer bonds yield more
  - Inverted: Predicts recession (short-term bonds yield more)

---

## 🧮 7. Financial Math (Simple but Key)

- **P&L = Value Today – Cost**
- **Risk = Std Dev of Return**
- **Sharpe Ratio = Return / Volatility**
  - Higher = better risk-adjusted performance
- **Hedge Ratio**: Offset exposure between assets

---

## 💡 8. Trading Logic by Role

### 🟢 Buy-Side (Asset Manager)
- Act on information faster than the market
- Use expected value:
  ```
  EV = (Chance of News Being True) × (Size of Price Move)
  ```
- Size trades based on conviction and volatility

### 🟡 Market Maker
- Make a tight bid/ask spread to earn profit per trade
- Widen spread in volatile conditions
- Hedge with correlated assets (e.g., long stock, short ETF)

### 🔵 Sales Trader
- Quote competitive prices with low risk
- Understand what client is trying to achieve
- Communicate news-driven logic persuasively

---

## 🎯 9. Terminology Cheat Sheet

| Term | Meaning |
|------|---------|
| Spread | Ask – Bid |
| Slippage | Loss due to poor execution |
| Correlation | How assets move together |
| Arbitrage | Riskless profit from price difference |
| VaR | Value at Risk (how much you could lose) |
| Delta | Sensitivity to price change |
| Beta | Volatility relative to market |

---

## 🧠 10. Real-Time Trading Mindset

- **Am I first, fast, or right?**
- **Is this already priced in?**
- **What’s my edge?**
- **Can I hedge this risk?**
- **How will others react to this news?**



## 📚 Recommended Reading / Watching (Fast Learning)

### 📘 Articles & PDFs
- [AmplifyME Knowledge Hub](https://amplifyme.com/resources) — Their official blog/videos.
- “The Basics of Financial Markets” – Investopedia [Free Starter Guide](https://www.investopedia.com/articles/basics/06/invest1000.asp)
- Summary PDFs:
  - Market Making (Investopedia)
  - [“A Beginner’s Guide to Trading Psychology” – IG.com](https://www.ig.com/en/trading-strategies/trading-psychology-200121)

### 🎥 YouTube Channels
- **AmplifyME** – Their videos directly match the simulator.
  - 🔍 Search: `AmplifyME Finance Accelerator Tutorial`
- **Two Cents** – Fast, visual finance education.
- **Bloomberg Quicktake** – Great for understanding market news.
- **Ben Felix / Plain Bagel** – Logical, no-hype finance explanations.

### 📘 Optional Books (Skim the right parts)
- *“Flash Boys” – Michael Lewis* (MM & speed)
- *“Trading for a Living” – Dr. Alexander Elder* (psychology + setup logic)
- *“The Psychology of Money” – Morgan Housel* (mindset)

---

## 🎯 Practice Mindset

- 🎮 **Simulator = Game**  
  → The goal isn’t to “guess right” but to **react fast + manage risk**.

- ⏱️ **Time Management**: Don’t freeze. Make fast, educated trades, and course-correct.

- 🧠 **Learn from Mistakes**: After each round, reflect on:
  - What news did I miss?
  - Was I too slow to act?
  - Did I hold a losing position too long?

