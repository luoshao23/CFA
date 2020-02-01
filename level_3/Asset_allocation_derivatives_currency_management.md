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

+ Delta ($\Delta$) = change in value of option / change in value of underlying, + for long call, - for long put
+ Gamma ($\Gamma$) = change in delta / change in value of underlying, + for long call and put
+ Vega ($\nu$) = change in value of option / change in volatitlity of underlying, + for long call and put
+ Theta ($\Theta$) = daily change in an option's price, - for long call and put

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