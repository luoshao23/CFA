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

### fixed-income futures

underlying: hyoothetical 30 year treasury bond with 6% coupon rate (why 6%?推出期货前后国债的收益率)

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
