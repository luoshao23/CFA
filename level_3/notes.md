### Yield Spread

+ N-Spread (Normal spread):
  + G-spread: the benchmark is government bond yield
  + I-spread: the benchmark is swap rate
+ Z-spread (Zero-volatility spread): is based on the entire benchmark spot curve. It is the constant spread that is added to each spot rate such that the present value of the cash flows matches the price of the bond.
+ OAS (Option-adjusted spread): is the Z-spread minus the theoretical value of the embedded call option
  + Callable bond: ZS（同等价格，但是假装不含权是的spread） > OAS（提出option后计算的spread）, 企业可以赎回债券，所以价格低
  + Putable bond: ZS < OAS, 投资者可以卖出债券，所以价格高

### Duration gap

+ if investment horizon > macaulay duration, then reinvestment risk dominates price risk, investor's risk is to lower interest rates;
+ if i = m, offset
+ if investment horizon < macaulay duration, then price risk dominates reinvestment risk, investor's risk is to higher interest rates;

### Interest rate risk

+ coupon reinvestment risk
+ market price risk

### Illustration on sources of return

+ hold a fixed-rate bond to maturity, reinvestment at YTM -> realzied return = YTM
+ sell prior to maturity, selling price priced at YTM -> realized return = YTM
+ hold a bond to maturity, reinvestment rate UP -> realized return > YTM, vice versa
+ hold for a short period (price risk dominates), reinvestment rate UP -> realized return < YTM
+ hold for a long period (reinvestment risk dominates), reinvestment rate DOWN -> realized return < YTM

### Macauly duration

$$\frac{dP}{dy}\frac{1}{P} = - \frac{1}{1 + y} \times Macauly\ Duration$$

$$Mac. D = \frac{[\frac{1C}{1 + y} + \frac{2C}{(1 + y)^2} + L + \frac{nC}{(1 + y)^n} + \frac{nM}{(1 + y)^n}]}{P}$$

So Mod. D = Mac. D / (1 + y)

### Duration

+ Duration is the slope of the price-yield curve at the bond's current YTM;
+ Duration is a weighted average of time (in years) until cash flow will received. The weights are proportions of the total bond value that each cash flow represents;
+ Duration is the approximate percentage change in price of 1% change in yield (price sensitivity).

Approximate modifief duration = $\frac{V_- - V_+}{2 \times V_0 \times \Delta YTM}$

Effective duration = $\frac{V_- - V_+}{2 \times V_0 \times \Delta curve}$

Price value of a basis (PVBP):

$$PVBP = P \times D \times 1bp$$

$$PVBP = \frac{V_- - V_+}{2}$$

### Convexity

Convexity is a mersure of the curvature of the price-yield curve.

approximate convexity = $\frac{V_- + V_+ - 2V_0}{(\Delta YTM)^2 V_0}$

effective convexity = $\frac{V_- + V_+ - 2V_0}{(\Delta curve)^2 V_0}$

### Key rate duration

+ 较小平行移动用 duration
+ 较大平行移动用 duration+convexity
+ 非平行移动用 key rate duration
+ 含权债券用 effective duration

### Return Attribution

Active return = return from factor tilts + security selection

### 个人IPS

RRTTLLU

+ Return
+ Risk tolerance
+ Time horizon
+ Taxes
+ Liquidity needs
+ Legal & Regulatory needs
+ Unique circumstances

### A valid benchmark is

SAMURAI

+ Specified in advance
+ Appropriate
+ Measurable
+ Unambiguous
+ Refective of current investment opinions
+ Accountable (Owned)
+ Investable


### Key features of hedge funds

+ lower regulatory and legal cosntraints, lack of transparency
+
+ flexible mandates
+ a large investment universe
+ aggressive investment exposures
+ comparatively free use of leverage
+
+ liquidity constraints for investors
+ higher cost structures

`cash drag`: 持有大额现金造成整体收益的降低

### 基金收费
+ management fee
+ incentive fees
  + high water mark
  + hurdle rate
    + soft hurdle rate: 只用于判断是否到达，整体收费
    + hard hurdle rate: 超额收益

### Classifiction of hedge fund strategies
+ Equity strategies
  + long/short equity: net long = long - short
  + short biased: focus on short, bottom-up, high Z-score(会不会破产清算) M-score(会计造假)
    + dedicated short-selling: 完全做空
    + short-biased
    + activist short selling: 看空+市场操纵
+ Equity market neutral: exposure 尽可能为0，适合市场环境不好的时候，short beta，high leverage，本身收益比较低
  + Pairs trading: 相关性较高的两个股票，long 低估，short 高估
  + Stub trading: 母公司、子公司，long 低估，short 高估
  + Multi Class: 不同资产，long 低估，short 高估
+ Event-Driven strategies: 存在event risk
  + soft-catalyst: 还没发生
  + hard-catalyst: 正在发生，风险较低
  +
  + merger arbitrage: 流动性较好，尤其对于hard-catalyst，杠杆较高，并购失败损失较大
    + cash-for-stock
    + stock-for-stock
  + distressed securities: 财务困境，买入低估的debt；购买进入重组公司的股票，杠杆较低
+ relative value: fixed-income
  + fixed-income arbitrage：高杠杆
    + duration
    + credit quality: AA v.s. BB
    + liquidty: on-the-run（新发行，流动性好） v.s. off-the-run（老债券）
    + optionality
    +
    + considering yield curve trades: yield steepness, 如果curve变陡，long 近期（因为yield 下降，价格要上升），short远期（因为yield 上升，价格要下降），同公司债券
    + carry trade: long on-the-run（新发行，流动性好） short off-the-run（老债券）, T-bond
  + convertible bond arbitrage: 买的人较少，低估，所以long undervalued 可转债，short overvalued 股票。存在流动性问题，高杠杆。high covertible issuance, moderate volatility, reasonable liquidity
+ opportunistic hedge fund strategies
  + global macro strategies: Top-down
  + managed futures: 风险因子
    + TSM: time series momentum, 依照上一个交易日
    + CSM: cross-sectional momentum, 产品间比较，相对好的long，差的short
  +
  + 相同点
    + 高杠杆
    + high volatility
    + high liquidity requirement
    + right tail
    + 分散化效果好
  + 不同点
    + Global macro: top-down
    + managed futures: 定量
+ Specialist strategies
  + volatility trading，买卖期权
    + time-zone: 同一产品，不同地区
    + cross-asset: 不同市场套利
  + reinsurance/ life settlements
    + 和市场相关性低，分散风险
+ Multi-Manager strategies
  + create one's own mix of managers by investing directly into HF
  + FOF
    + diversification
    + 小投资
    + low tail risk
    + 费率结构复杂
    + 杠杆高
  + Multi-strategy funds
    + 费率结构简单
    + TAA效率高
    + transparency 高
    + operational risk 高
    + left tail， risk高

### Conditional factor risk model

following four factors

1. Equity risk, SNP500
2. Currency risk, USD
3. Credit risk, CREDIT
4. Volatitility, VIX

+ Sharp ratio: $(R_p - R_f) / sigma_p$
+ Sortino ratio*: $(R_p - MAR) / Downside\ risk$

*MAR = 最低期望收益率

### Trade strategy input

+ order characteristics
  + side: liquidity demander take longer time
  + size
  + relative size: % of ADV (average daily volume)
+ security characteristics
  + security type
  + short-term alpha: 越紧急交易成本越高
  + price volatility: market impact v.s. execution risk
  + security liquidity
+ market conditions
  + liquidity crises: 金融危机；从指数中剔除出来会减少流动性
+ User-based considerations: trading cost risk aversion
+ market impact and execution risk

### reference price

determing trade prices for execution strategy and calculating actual trade costs

+ pre-trade benchmarks
  + decision price: 决策价格, 理论价格，偏量化
  + previous close: 前一天收盘价格，偏量化
  + opening price: 基本面分析师，较稳定，提出隔夜风险
  + arrival price: 交易比较紧急
+ intraday benchmark: 平均价格
  + VMAP(volume-weighted average price): 上一个交易日按时间切分，每个时间的交易量及价格的加权平均，易受异常值影响
  + TWAP(time-weighted average price): 上一个交易日按时间切分，每个时间段价格的算术平均，剔除异常值
+ post-trade benchmark
  + closing price: passive management，最小化追踪风险
+ price target benchmark: 定制化，短期alpha，自己定

### trade strategies

+ short-term alpha: urgency
+ long-term alpha: low trade urgency
+ risk rebalance: 调整权重
+ cash flow driven - redemption: 流出
+ cash flow driven - equitization: 资金流出，股权化

### trade execution

+ trade implementation choices
  + higher-touch approaches: 流动性比较差
    + `principal trades`: 做市商dealer
    + `agency trades`: broker市场
    + 场外dealer: request for quote (RFQ)
  + automated execution approaches
    + ATS(Alternative trading systems)：场外
    + DMA(Direct market access): 直接市场准入，derivatives and currency
    + dark pools: 暗市交易，防止信息泄露，交易时间可能很长
+ algorithmic trading
+ comparsion of markets

### Equity return attribution

Carhart four-factor model

$$R_p = R_f + \alpha + b_1 RMRF + b_2 SMB + b_3 HML + b_4 WML + E_p$$

+ RMRF = the return on a value-weighted equity index inexcess of the one-month T-bill rate
+ SMB = small minus big, size factor
+ HML = high mius low, a value factor, high means high-book-to-market(价值型股票)
+ WML = winner minus losers, a momentum factor
+ $E_p$ = an error return
+ b1 = 1, average market risk
+ b2 > 0, 偏向小盘股
+ b3 > 0, 偏向价值股
+ b4 > 0, 追涨杀跌

### yield-curve decomposition

+ yield
+ roll: 持仓变动
+ shift: 收益率曲线平行移动
+ slope: 斜率
+ curvature
+ credit spread
+ specific: 个体债券
+ residual

### Properties of a valid benchmark - SAMURAI

+ Specified in advance
+ Appropriate
+ Measuerable
+ Unambiguous: benchmark 成分明晰
+ Reflective of current investment opinions: 超配的股数越多越反应基金经理的观点
+ Accountable: 双方都是认可的
+ Investable: 可以直接复制投资