# Asset allocation derivatives and currency management

## derivative preview

+ moneyness
  + in the money: positive payoff
  + at the money: no payoff
  + out of the money: negative payoff
+ option value = intrinsic value + time value
+ BSM model
    $$C_0 = [S_0 \times N(d_1)] - [X \times e^{-R_f^c \times T} \times N(d_2)]$$
+ factors affect the value of an option, $P_{option} = f(S, X, T, r_f, \sigma)$

  | sensitivity factor | calls | puts |
  | ------------------ | ----- | ---- |
  | underlying price   |  +    |  -   |
  | volatiltity        |  +    |  +   |
  | risk-free rate     |  +    |  -   |
  | time to expiration |  +    |  +*  |
  | strike price       |  -    |  +   |
  | payments on the underlying  |  -    |  +   |
  | carrying cost      |  +    |  -   |

  exception: european put option which is deep-in-money, thetas are negative

+ volatility
  + historical: $\sigma = \sqrt{S_{R_i^c}^2} = \sqrt{\frac{\sum_{i=1}^N (R_i^c - \bar{R_i^c})^2}{N - 1}}$
  + implied: 根据市场价格倒推
+ put call parity
  $$c + \frac{X}{(1 + R_f)^T} = S + p$$

  + protective put: S + p
  + fiduciary call: $c + X/(1+R_f)^T$

## Synthetic Asset

+ synthetic long/short forward
  + long call + short put = long forward
  + long put + short call = short forward
+ sythetic call/put
  + long call = long asset + long put
  + long put = short asset + long call

## covered calls and protective puts

+ covered call = S - call, 认为标的资产会上涨
  + yield enhancement, 一般write OTM call option, 大概率不实现, 赚期权费
  + reducing a position at a favorable price, 当前想减仓, 一般write ITM call option
  + target price realization, hybrid of the previous two, OTM call option
+ protective put = S + put
  + 和止损单相比，止损单可能低开无法达到target，所在价格的交易股数有限，protective put可以在target price成交期望的股数，但是有时间限制，且有费用
+ Delta of the strategy
  + delta of covered call = delta of stock - delta of call stock
  + delta of protective put = delta of stock + delta of put stock
+ cash secured put = put + K/(1+r_f)^T

### investment objectives of covered calls

covered call profit at expiratin = $S_T - Max[(S_T - X), 0] + c_0 - S_0$

maximum gain = $X - S_0 + c_0$

maximum loss = $S_0 - c_0$

Breakeven price = $S_0 - c_0$

Expiration value = $S_T - Max[(S_T - X), 0]$

Profit at expiration = $S_T - Max[(S_T - X), 0] + c_0 - S_0$

### investment objectives of protective puts

protective put profit at expiration = $S_T + Max[(X - S_T), 0] - S_0 - p_0$

maximum gain = $S_T - S_0 - p_0$ = Unlimited

maximum loss = $S_0 - X + p_0$

Breakeven price = $S_0 + p_0$

Expiration value = $S_T + Max[(X - S_T), 0]$

Profit at expiration = $S_T + Max[(X - S_T), 0] - p_0 - S_0$

## collars

collars = covered call + protective put

profit at expiration = $S_T + max(0, X_L - S_T) - max(0, S_T - X_H) - S_0 - p_0 + c_0$

maximum gain = $S_T + 0 - (S_T - X_H) - S_0 - p_0 + c_0 = X_H - S_0 - p_0 + c_0$

maximum loss = $S_T + (X_L - S_T) - 0 - S_0 - p_0 + c_0 = X_L - S_0 - p_0 + c_0$

mid range(i.e., if $X_L < S_T < X_H$) = $S_T + 0 - 0 - S_0 - p_0 + c_0 = S_T - S_0 - p_0 + c_0$

Breakeven price (if exists) = $S_0 + p_0 - c_0$

## spreads

### Bull spread (小涨)

+ call spread: 牛市用call顺势而为，$call_L - call_H - c_L + c_H$
+ put spread: 牛市用put赚premium，$-put_H + put_L + p_H - p_L$

### Bear spread (小跌)

+ put spread: 熊市用put顺势而为，$put_H - put_L - p_H + p_L$
+ call spread: 熊市用call赚premium，$-call_L + call_H + c_L - c_H$

### calendar spread

\- near-dated call + longer-dated one

## straddle

*put + call* at same **exercise price** and same **expiration date**, on same **underlying asset**

## option Greeks

+ Delta ($\Delta$) = change in value of option / change in value of underlying, + for long call, - for long put
  + call delta 0->1 when stock price increases
  + put delta -1->0 when stock price increases
  + $\Delta = N(d_1)$ for call, and $\Delta = N(d_1) - 1$ for put
+ Gamma ($\Gamma$) = change in delta / change in value of underlying, + for long call and put
  + Gamma = $\Delta delta / \Delta S$
  + call and put options on the same stock with the same T and X have equal gamma
  + Gamma is largest when the option is **at-the-money** or **near expiration**
  + if the option is deep in- or out- of the money, gamma approaches 0.
+ Vega ($\nu$) = change in value of option / change in volatitlity of underlying, + for long call and put
+ Theta ($\Theta$) = daily change in an option's price, - for long call and put
+ Rho ($\Rho$), + for call, - for put
  + small impact compared to vega

## implied volatility and volatility skew

`volatility smile`: the implied volatility is relatively low for **at-the-money** options. It becomes progressively higher as an option moves either **into the money or out of the money**.

`volatility skew` (smirk): the volatility used to price a **low-strike-price** option is significantly higher than that used to price a **high-strike-pirce** option (especially **equity** options)

### why smirk?

+ leverage (equity price -> volatility), companies become more risky
+ volatility feedback effect (volatility -> equity price), investors require a high return when price declines
+ *crashophobia* (expected equity-> implied volatility), 恐慌

### strategy

因为低价的风险高估，所以**long call and short put**，但存在下行风险 a long exposure to the underlying

### alternative ways of characterizing the volatility smile

+ K/S_0 or K/F_0
+ delta

### volatility surfaces

+ implied volatility tends to be an increasing fucniton of maturity when short-dated volitilities are historically low
+ implied volatility tends to be an decreaing fucniton of maturity when short-dated volitilities are historically high

$$\sigma_{Annual}(\%) = \sigma_{Monthly}(\%) \sqrt{\frac{252}{21}}$$

### criteria for identifying appropriate option strategies

|  |  | Bearish | Neutral View | Bullish |
|---|---|------|--------|---------|
| Expected Move in Implied Volatility | Decrease | Write calls | Write straddle | Write puts |
|  | Remain Unchanged | Write calls and buy puts | Calendar spread | Buy calls and write puts |
|  | Increase | Buy puts | Buy straddle | Buy calls |

## interest rate risk

### interest rate swap

for individual assets and liabilities, the tradeoff is between the market value risk associated with fixed rates and the cash flow risk associated with floating rates

interest rate swaps can be used to

+ convert between floating exposure and fixed exposure

    | existing exposure | converting | interest rate swap required | beneficial when |
    | ------| ------- | ------- | -------- |
    | floating-rate liability | floating to fixed | payer swap | floating rates expected to rise |
    | fixed-rate liability | fixed to floating | recerver swap | flaoting rates expected to fall |
    | floating-rate asset | floating to fixed | receiver swap | floating rates expected to fall |
    | fixed-rate asset | fixed to floating | payer swap | floating rates expected to rise |
+ alter the duration of a fixed-income protfolio

  + **duration** = $duration_{receive} - duration_{pay}$
  + A pay-fixed, receive-floating swap has a negative (positive) duration from the perspective of a fixed-rate payer
  + for fixed-rate side, duration is approximately **0.75**
  + for floating-rate side, reset period 0.5 or average 0.5*1/2 = 0.25
  + the portfolio manager can achieve a combination of the existing portfolio and the interest rate swap that sets the overall protfolio duation to the target dutation:
    $$MV_P \cdot MDUR_P + N_S \cdot MDUR_S = MV_P \cdot MDUR_T$$

    or

    $$N_S = \frac{MDUR_T - MDUR_P}{MDUR_S} MV_P$$

### Forward rate agreement (FRA)

A forward rate agreement is an OTC derivative instruemnt that is used mainly to hedge a loan expected to be taken out in the near future or to hedge against changes in the level of interest rates in the future.

可能会违约

### Short-term interest rate (STIR) futures

+ Eurodollar futures 报价 100 - annualized forward rate
+ the pricing convention means that futures prices will rise when forward rates fall
+ one basis point change in the forward rate will cause the contract's value to change by $25 ($1 million * 0.0001 (1bps) * 90/360 = $25)

#### Eurodollar futures v.s. FRA

+ a long Eurodollar futures position will increase in value as forward rates decrease, and decrease in value as forward rates increase，场内，基本无违约风险，标准化
+ a long FRA position, which increase in value as forward rates increase, and decrease in value as forward rares decrease，场外，有违约风险，可以任意定制
+ borrower long FRA, short Eurodollar futures
+ lender short FRA, long Eurodollar

why? 一个是利率，一个报价是100-利率

+ both eurodollar futures and FRA agreements allow lenders and borrowers to lock in rates for future borrowing and lending

### fixed-income futures (长期！)

underlying: hypothetical 30 year treasury bond with 6% coupon rate (why 6%?推出期货前后国债的收益率)

T-bills: < 1 year; Treasury notes: < 10 years; Treasury bonds: < 30 years

虚拟债券，实体交割，实际债券由卖方决定，防止逼空（即买方自己囤积该类债券做多，然后让卖方按该类债券交割）。故卖方交割CTD(cheapest-to-deliver) bond, bond can be deliverable: $100000 par value T-bonds with any coupon with a maturity of at least 15 years.

for a specific bond A: $FP_f = FP_A \times \frac{1}{CF_A}$ or $FP_A = CF_A \times FP_f$

$$N = \frac{D_T - D_P}{D_f} \cdot \frac{P_\$}{f_\$} = \frac{D_T - D_P}{D_{CTD} / CF_{CTD}} \cdot \frac{P_\$}{f_\$} = \frac{BPV_T - BPV_P}{BPV_{CTD}} CF_{CTD}$$

a.k.a.,

$$HR = \frac{\Delta P}{\Delta CTD} CF$$

$$BPVHR = \frac{-BPV_P}{BPV_{CTD}} CF$$

### Equity swaps

An equity swap is used to convert the returns from an equity investment into another series of returns, which either can be derived from another equity series or can be a fixed rate.

`!Note`: 可能出现双收双支

+ receive-equity return, pay-fixed
+ receive-equity return, pay-floating;
+ receive-equity return, pay-another equity return

The equity return may include dividend return plus price return based on

+ a single stock
+ a basket of equities
+ an equity index

### Equity forwards and futures

$$N_f = \frac{\beta_T - \beta_S}{\beta_f} \frac{MV_P}{F} = \frac{\beta_T - \beta_S}{\beta_f} \frac{MV_P}{f \times multiplier}$$

+ synthetic risk-free asset = Long stock - stock index future
  $$N_f = \frac{- \beta_S}{\beta_f} \frac{MV_P}{F}$$
+ synthetic equity = Long risk-free asset + stock index future
  $$N_f = \frac{\beta_T}{\beta_f} \frac{MV_P}{F}$$

### currency swap

reason for currency swap:

+ converting a loan in one currency into a loan in another currency
  + cross-currency basis swap: in which **notional principals are exchanged** because the goal of the transaction is to issue at a more favorable funding rate and swap the amount back to the currency choice
+ converting foreign cash receipts into domestic currency
  + synthetic borrowing **with no principal**

### currency forwards

HR = Amount of currency to be exchanged / Futures contract size

### Derivatives on volatility

VIX index measures implied volatitlity in the S&P 500 Index over a forward period of 30 days.

As VIX returns and equity returns are mostly negatively correlated. VIX is known as the fear index or fear guage as we can directly view the market's expectation of future volatility.

VIX value is the annualized standard deviation of the expected percentage moves in the S&P 500 Index over the following 30 days.

+ VIX futures
  + cannot invest in spot VIX
+ VIX option
  + cash-settled European-style
+ Variance swaps
  + realized variance = $252 \times [\sum_{i=1}^{N-1} R_i^2 / (N-1)]$, where $R_i = ln(P_{i+1}/P_i)$ and N is the number of days observed
  + variance notional = vega notional / 2K
  + settlement amount = $N_{Vega}(\frac{\sigma^2 - X^2}{2K}) = N_{variance}(\sigma^2 - X^2)$
  + market-to-market valuation:
    $$V_t = PV_t\{variance\ notional \times (\frac{t}{T}[RealizedVol(0,t)]^2 + \frac{T-t}{T}[ImpliedVol(t,T)]^2 - K^2)\}$$
+ Fed Funds
  + Fed funds futures contract price = 100 - Expected FFE rate
  + 25 bps "target range"
  + Prob = (effective Fed funds rate implied - current Fed funds rate) / (Fed funds rate assuming a rate hike - current Fed funds rate)

## Currency Managemenet

+ 直接报价 A/B, B为考察对象, DC/FC = P/B
+ Bid/Asked Rule: bid(low)/ask(high) = buy/sell (for dealer)
+ Forward points: divide 10000
+ market-to-market value: (FP_t - FP)(contract size)/(1 + R(days/360))

### FX swap

> 先close原先的swap，再long一个新的下一期swap

Similar to currency swaps, FX swaps involve an exchange of principal amounts in different currencies at swap initiation that is reversed at swap maturity.

Unlike currency swaps, FX swaps have no interim interest payments and are nearly always of much shorter term than currency swaps.

Interest rate parity: $\frac{F}{S} = \frac{1 + r_{DC}}{1 + r_{FC}}$

### Return decomposition

$$R_{DC} = (1 + R_{FC})(1 + R_{FX}) - 1$$

where $R_DC$ is the domestic-currency return (in percent), $R_FC$ is the foreign-currency return, and $R_{FX}$ is the percent change of the foreign currency against the domestic currency

$$R_{DC} = \sum_{i=1}^n \omega_i (1 + R_{FC, i})(1 + R_{FX, i}) - 1$$

where $\omega_i$ are the portfolio weights of the foreign-currency assets (defined as the percent of the aggregate domestic-currency value of the portfolio) and $\sum_{i = 1}^n \omega_i = 1$

### Volatility decomposition

$$R_{DC} = (1 + R_{FC})(1 + R_{FX}) - 1 = R_{FC} + R_{FX} + R_{FC}R_{FX} \approx R_{FC} + R_{FX}$$

we have combination equation of volatility:

$$\sigma^2(\omega_x X + \omega_y Y) = \omega_x^2\sigma^2(X) + \omega_y^2\sigma^2(Y) + 2 \omega_x \omega_y \rho(X, Y) \sigma(X) \sigma(Y)$$

since holding a foreign asset is equivalent to holding foreign currency and foreign equity at the same time, so

$$\sigma^2(R_{DC}) = \sigma^2(R_{FC}) + \sigma^2(R_{FX}) + 2 \rho(R_{FC}, R_{FX}) \sigma(R_{FC}) \sigma(R_{FX})$$

出口型公司 本币下跌，股票上升；进口型公司 本币上升，股票上升；

if $R_{FC}$ is a risk-free return:

$$\sigma(R_{DC}) = (1 + R_{FC})\sigma(R_{FX})$$

### strategic currency management

+ long run currency effects cancel out to zero due to: (不hedge)
  + exchange rates revert to historical means or their fundamental values
  + an efficient currency market is a zero-sum game
  + management and transaction costs
+ can have a dramatic impact on short-run returns and return volatility: 短期hedge长期不hedge
  + there are pricing inefficiencies in currency markets
  + much of the flow in currency markets is related to international trade or capital flows in which FX trading is being done on a need-to-do basis and these currency trades are just a spinoff of the other transactions
  + some market participants are either not in the market on a purely profit-oriented basis (e.g., central banks, government agencies) or are believed to be uniformed traders

### the IPS

most IPS specify many of the following points: 要在IPS中说好如何hedge风险

+ general objectives of the invesment protfolio
+ the risk tolerance of the porfolio and its capacit for beaing risk
+ the time horizon over which the portfolio is to be invested
+ the ongoing income/liquidity needs (if any) of the portfolio
+ the benchmanrk against which the portfolio iwll measure overall investment returns

the currency risk management policy will usually address such issue as

+ target proportion of currency exposure to be passively hedged（和benchmark一样hedge）
+ latitude for active currency management around this target
+ frequency of hedge rebalancing
+ currency hedge performance benchmark to be used
+ hedging tools permitted

### choice of currency exposure

#### diversification considerations

+ 长期不用hedge，短期要hedge
+ negative correlation不用hedge，positive要
+ depend on market conditions and longer-term trands in currency pairs
+ fixed-income(和利率相关性更大) 更需要hedge than equity portfolios
+ hedge ratios vary widely in practice among different investors

#### cost consideration

+ trading expenses is expensive
+ if the options expire out of money, this cost is unrecoverable
+ rolled forward with an FX swap to maintain the hedge. rolling hedges will typically generate cash inflows or outflows (roll时会调整金额)
+ maintain an administrative infrastructure
+ opportunity cost of the hedge:
  + split the difference and have a 50% hedge ratio
  + not to hedge every minor, daily change, but only the larger adverse movements

#### choice of currency management strategies

1. passive hedging
   + benchmark
   + rules-based approach
2. discretionary hedging (自主)
   + the primary duty is to protect the portfolio from currency risk 降风险
3. active currency management
   + the active currency manager is supposed to take currency risks and mange them for profit 原有基金经理在原来货币上追求收益
4. currency overlay used differently by different sources, 外汇视为单独资产大类，进行积极投资，可以在任意货币追求收益
   + hired currency overlay manager
   + sometimes a distinciton is made between currency overlay and foreign exchange as an asset class

#### formulatinh a currency mgt. program

the strategic currency positioning of the portfolio should be biased toward a more-fully hedged currency management program the more:

+ short term
+ rsik averse
+ immediate the incomme and/or liquidity needs
+ fixed-income assets
+ cheaply a hedging program can be implemented
+ volatile financial markets are
+ skeptical the beneficial owners are of the expected benefits of active currency management

## active (tactical) currency management

tactival decision involve active currency management based on

+ economic fundamentals
  + all else equal, the base currency's real exchange rate should appreciate if there is an upward movement in:
    + long-run equilibrium real exchange rate
    + its real or nominal interest rates, which should attract foreign capital
    + expected foreign inflation, which should cause the foreign currency to depreciate
    + the foreign risk premium, which should make foreign assets less attractive compared with the base currency nation;s domestic assets
+ technical analysis
+ carry trade
  + covered interest rate parity (CRIP):
    $$\frac{F_{P/B} - S_{P/B}}{S_{P/B}} = \frac{(i_P - i_B)(t/360)}{1+i_B(t/360)}$$
  + if uncovered interest rate parity holds, 高收益会被贬值抵消，无意义。但是历史数据表明，短期存在deviation
  + leverage involved magnifying their losses
  + lower volatility is better for a carry trade position. if implied volatility rises, close the trade
  + often referred to as the forward rate bias
    + carry trade: 借入低利率A，换成高利率B，即现货市场卖A买B
    + forward rate bias: A低利率所以远期合约是溢价，B高利率所以远期折价，现货市场卖出A买入B

    |  | Buy/invest | Sell/borrow |
    |--|-----|----|
    |Implementing the carry trade | high-yield currency | low-yield currency |
    |Trading the forward rate bias | forward discount currency | forward premium currency |

+ volatility trading
  + strangle: a variation on a straddle in which the put and call have different exercise prices, 便宜，更难赚钱

#### Factors affect tactical trading decision

| Expectations |  | Actions |   |
| --- | --- | --- | ----|
| Relative currency | Appreciation | Reduce the hedge or increase the long position in the currency |
| Relative currency | Depreciation | Increase the hedge or decrease the long position in the currency |
| Volatility | rising | long straddle (or strangle) |
| Volatility | failing | short straddle (or strangle) |
| market conditions | stable | a carry trade |
| market conditions | crisis | discontinue a carry trade |

### Tools of currency management

+ forward contract (优于futures)
  + not standardized
  + futures contracts may not always be available in the currency pair that portfolio manager wants to hedge
  + futures require initial margin and ongoing margin
  + daily trade volume larger than futures
  + roll yield (also roll return, carry trade) is given by
    $$\frac{F_{P/B} - S_{P/B}}{S_{P/B}}$$


  + consideration of static/dynamic hedge
    + cost-benefit trade-offs
    + higher the degree of risk aversion, more dynamic
    + the greater the tolerance for acvtive trading, and the stronger the commitment to a particular market view (more static)
+ currency option
+ strategies to reduce hedging costs and modify a portfolio's risk profile
  + over-/under-hedging using forward contracts
  + protective put using OTM options
  + risk reversal (or collar)
  + put spread
  + seagull spread (下跌风险打开，但是可以赚期权费)
    + a bull call spread - OTM put
    + a bear put spread - OTM call
  + exotic options (奇异期权)
    + knock-in(生效): up-in/down-in
    + knock-out(失效): up-out/down-out
    + binary option(digital option): pay fixed amount if condition meets

### hedging multiple foreign currencies

must consider the correlation between the various foreign-currency risk exposures, e.g., AUZ and NZD

+ cross hedge (proxy hedge)
  + normally, no need, since forward can be customized
  + however, if the portfolio already has "natural" cross hedges
+ macro hedge: 一揽子货币综合考虑
+ Minimum-Variance hedge ratio (MVHR):
  $$\frac{cov(y, x)}{var(x)} = corr(y, x) \times \frac{std(y)}{std(x)}$$
+ basis risk: the risk resulting from using a hedging instrument that is imperfectly matched to the investment being hedged，使用的工具和要对冲的标的不完全一致
  + not perfectly correlated
  + correlation will change with time

### basic intuitions for using currency Mgt. tool

+ not a free good
+ cost vary depending on condition
+ cost is focused on its core
  + writing options to gain upfront premiums
  + varying the strike prices
  + varying notional amounts
  + using exotic features
+ reduced cost : residual risk, 风险与收益并存
+ natural hedges
+ no single or best way to hedge