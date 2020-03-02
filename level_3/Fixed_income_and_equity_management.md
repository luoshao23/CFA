> three specific bond portfolio:

+ Laddered Portfolio: 每期都有现金流，dispersion中等
+ Bullet portfolio: 现金流集中在中期，dispersion最小
+ Barbell portfolio: 现金流集中在短期和长期两端，dispersion最大

$$convexity = \frac{MacD^2 + MacD + Dispersion}{(1 + yield)^2}$$

dispersion（方差）越大，convexity越大，structural risk越大

## roles of fixed-income in portfolios

+ diversification benefits
  + correlation between 投资级（国债）and equity 较低
  + correlation between 投机级（公司债）and equity 较高
  + 全球投资correlation更小
  + correlation is not constant
    + market stress period
      + decrease between government and equity
      + increase between high yield bond and equity
  + bonds less volatile than equity: near-term(政策影响) volatility > average volatility
+ produce regular cash flows
  + meet future obligations
    + tuition(学费) payments
    + pension obligations
    + payout on life insurance policies
  + approach: ladder bond porfolio by staggering the maturity dates of portfolio bonds through investment horizon: **balance price risk and reinvestment risk**
+ a hedge for inflation
  + $R_{nominal} = Real + inflation rate$
  + protection against inflation

    |    |  coupon  | principal |
    | --- | ---- | ----|
    |fixed-coupon bonds | unprotected | unprotected |
    |floating-coupon bonds | protected | unprotected |
    |inflation-linked bonds (i.e., TIPS) | protected | protected |

## fixed-income mandates

liability-based mandates (or Asset liability management (ALM)/ structured mandates/ Liability-driven investment (LDI)) and total return mandates (or AO)

+ ALM
  + user of liability-based mandates:
    + individual: funding cash flow & life style needs
    + institution: bank, insurance, pension funds
  + duration matching
    + 假设: yield curve 平行移动
    + 条件:
      + the present value of the bond porfolio's assets must equal the present value of the liabilities $PV_A = PV_L$ and
      + a bond portfolio;s duration must equal the duration of the liability portfolio $D_A = D_L$,
      + convexity 越小越好，因为yield curve risk变小, i.e., convexity_A > convexity_L
      + i.e., $PV_A \times D_A = PV_L \times D_L = DollarD_A = DollarD_L$

    + risk:
      + interest rate risk, 因为忽略了convexity
      + yield curve risk, 非平行移动
      + rebalancing risk
    + other consideration
      + rebalance periodically
      + liquidity considerations, may need to be liquidated in order to satisfy the liability outflows
      + high portfolio turnover
      + not default
      + bonds with embedded options, better measured by effective duration
  + cash flow match
    + 无假设
  + comparison between duration match and cash flow match

    |  | duration | cash flow match |
    |-----------|--------|----------|
    | yield curve assumption | parrallel yield curve shifts | None |
    | mechanism | risk of shortfall in cash flows is minimized by matching duration and present value of lliability stream | Bond portfolio cash flows match liabilities |
    | basic principle | cash flows come from coupon and principal repauments of the bond portfolio and offset liability cash flows | cash flow, coupon and principal repayments of the bond portfolio offset liability cash flows |
    | rebalancing | frequent rebalancing required | not required but often desirable |
    | complexity | high | low |

  + contingent immunization
    + when value of asset portfolio > present value of liability -> surplus -> allowed to actively manage the asset portfolio
    + when actively managed portfolio < specified threshold -> active management ceases
  + horizon matching
    + cash flow matching (short term, <= 4-5 years) + duration matching (long term)
+ Total return mandates (AO)

  |          | pure indexing | enhanced indexing | active management |
  | ---------| ------------- | ----------------- | ----------------- |
  | objective | match benchmark return and risk as closely as possible | modest performance (20-30bp) of benchmark while active risk is kept low (around 50bps or lower)| higher outperformance (50bps or more) of benchmark and higher active risk levels |
  | portfolio | same as benchmark or only slight mismatches | small deviations from underlying benchmark | significant deviations from underlying benchmark |
  | risk | risk factors are matched exactly | most primary risk factors are closely matched (duration) | deviations from benchmark (duration)|
  | turnover | similar to underlying benchmark | slighly higher then underlying benchmark | considerably higher turnover than the benchmark |

### DB plan

+ accumlated benefit obligation (ABO):
  $$ABO = \frac{1}{(1+r)^T} \times [\frac{m \times G \times W_0}{1+r} + \frac{m\times G \times W_0}{(1+r)^2} + ... + \frac{m \times G\times W_0}{(1+r)^Z}]$$
+ projected benefit obligation (PBO):
  $$PBO = \frac{1}{(1+r)^T} \times [\frac{m \times G \times W_T}{1+r} + \frac{m\times G \times W_T}{(1+r)^2} + ... + \frac{m \times G\times W_T}{(1+r)^Z}]$$
+ effective duration
  $$\frac{(PV_-) - (PV_+)}{2 \times \Delta Curve \times (PV_0)}$$
+ interest rate swap
  $$Asset\ BPV + [NP \times \frac{Swap\ BPV}{100}] = Liability\ BPV$$

## bond market liquidity

fixed-income securities vary greately in their liquidity

+ v.s. equity markets: less liquid & less transparent
+ on-the-run liquidity > off-the-run liquidity
+ liquidity decrease -> yield increase

### liquidity among bond market sub-sectors

| | more liquidity | less liquidity | reason |
|--|---|---|---|
| issuers | sovereign goverment bond | corporate and non-sovereign government bond | + issuance size; + use as benchmark bond; + acceptance as collateral in repo market; + well-recognized issuers |
| credit quality | high | lower | find a counterparty dealer |
| issue frequency | outstanding issue | infrequent issuers | familarity |
| issue size | larger issues | smaller issues | include or excluded in/from bond index with minimum issue size requirements |
| maturity | nearer-term bonds | longer maturities bonds | intent to hold them until maturity |

### the effects of liquidity on fixed-income portfolio management

+ pricing
  + electronic systems help to increase tranparency
  + matrix pricing: 线性差值
    + advantage: no require complex financail modeling
    + disadvantage: ignore some value-relevent features between bonds
+ portfolio construction
  + trade-off between **yield** and **liquidity**
  + 2 types of investors
    + buy-and-hold: prefer less liquid bonds for higher yields
    + investors that emphasize liquidity, give up some yield
  + dealer market
    + lower bid-ask spread (higher liquidity)
    + higher bid-ask spread (lower liquidity)

### alternatives to direct investment in bonds

+ fixed-income derivative
  + futures, forward, options
  + swaps: interest rate swaps, CDS
+ fixed-income ETF and pooled investment vehicles

## a model for fixed-income returns

### decomposing expected returns

$$E(R) \approx yield\ income
+ rolldown\ return
+ E(change\ in\ price\ based\ on\ investor's\ views\ of\ yields\ and\ yield\ spreads)
- E(credit\ losses)
+ E(currency\ gain\ or\ losses)$$

+ yield income
  $$yield\ income = \frac{annual\ coupon\ payment}{current\ bond\ price} = \frac{coupon + reinvestment\ income}{current\ bond\ price}$$

+ rolldown return (利率不变，时间变): assuming an unchanged yield curve
  $$rolldown\ return = \frac{bond\ price_{end} - bond\ price_{beginning}}{bond\ price_{beginning}}$$

+ roll yield = yield income + rolldown return
+ E(chang in price based on investor's views of yields and yield spreads) (利率变) = [-MD * dYield] + [1/2 * convexity * (dYield)^2]
+ E(credit losses) = P(default) * expected loss severity (loss given default)
+ E(currency gain or losses), generally given

## leverage

`leverage` is the use of borrowed capital to increase the magnitude of portfolio positions

$$R_E = R_A + \frac{B}{E}(R_A - R_B)$$

where $R_A$ = total portfolio return, $R_E$ =  return on equity, $R_B$ = borrowing return

### Methods for leveraging fixed-income portfolios

+ futures contracts
  $$Leverage_{futures} = \frac{Notional value - margin}{margin}$$
+ swap agreement
+ structured financial instruments
+ repurchase agreement

  dollar interest = principal amount * repo rate * (term pf repo in days / 360)
+ securities lending

  the portion of the collateral earnings rate that is repaid to the security borrower by the security lender

  rebate rate = collateral earning rate - security lending rate

## taxation


## liability-driven and index-absed strategies

ALM

+ ADL, assets are given and liabilities are structured to manage interest rate risk
+ LDI (important), liabilityies are given and assets are managed

|  | Type I | Type II | Type III | Type IV |
|--|----|----|----|----|
|cash outlay amount | known | known | unknown | unknown |
|timing | known | unknown | known | unknown |
|example | fixed income, bond having no embedded options | callable bond, putable bond, term life insurance | floating rate note, structure notes have principal inflation indexed bonds | property and casulaty insurance (财险车险), company DB plan |

## interest rate immunization

key assumption: sufficient but not necessary condition: a parallel yield curve shift

convexity = (macaulay duration^2 + macaulay duration + dipersion) / (1 + cash flow yield)^2

## multiple liabilities

+ duration money

### risk in LDI

+ model risk
+ interest rate risk: convexity
+ yield curve risk: non-parallel
+ spread risk
  + immunizing multiple type I liabilities
  + derivatives overlay LDI strategies
  + interest rqate swap overlays
+ conterparty credit risk
+ collateral exhaustion risk
+ liquidity risk

## matching a FI portfolio to an index

+ pure indexing: replicate an existing mmarket index by purchasing all of the constituent securities in the index to minimize tracking risk
+ enhanced indexing strategy: the investor purchases fewer securities than the full set of index constituents but matches primary risk factors reflected in the index
+ active management
+ tracking risk
  + tracking error: the standard deviation of a porfolio's active return for a given period, and active return is defined as
  + active return = portfolio return - benchmark index return

### fixed income market

+ unique characteristics which make them difficult to track
+ investors face significant challenges in replicating a bond market index
  + size and breadth
  + wide array
  + unique issuance and trading pattern

### passive investment

mimic the prevailing characteristics of the overall investment available in terms of credit quility types of borrower maturity, and duration rather than express a specific marktet view

+ consistent with efficient market theory
+ replicate the market performance rather than outperform the market
+ bond market index replication
  + most straght forward
  + breif that active manafer cannot outperform the index
  + do not require manger analysis
  + task is to purchase or sell bonds when index changes and in/outflows
  + advanteges: best means of diversification
  + disadvantage: neither feasible nor cost-effective

alternative methods for passive investment

1. mutual fund
   + pooled invesment vehicles
   + open-ended mutal fund: NAV at the end of each trading day
2. ETF
   + more tradability
   + NAV of the underlying bonds
3. Total return swap (TRS): 期初无头寸
   + advantage: no requiring of the full cash outlay
   + disadvantage: not actually own the underlying assets

### enhanced indeixng strategy

+ the goal of the approach:
  + mirror the most important index characteristics
  + closely track index performance
+ more efficient

#### stratified sampling

steps:

1. 分类分层
2. manager identifies a subset of bonds with each correspinding index cell
3. positions in each cell are adjusted over time

Environmental, social, and corporate governance ESG

enhanced strategies:

1. lower cost enhanceent
2. issue selection enhancement: by using bond valuation models
3. yiled curve enhancement
4. sector/ quality enhancements: 看经济形势
   1. 周期/非周期行业
   2. 质量好/差
5. call exposure enhancement
   1. 利率低，少配含权债
   2. 利率高，多配含权债

#### primary indexing risk factors

primary indexing risk factors as follows:

1. portfolio modified adjusted duraiton (interest rate risk): effective duration
2. key rate duration (yield curve risk)
   1. zero coupon bond: key rate duration
   2. coupon paying bond: present value of distribution of cash flows methodology (PVD), 多个coupon paying bond 转变为多个zero coupon bond，权重为每个zero coupon bond的现值的权重，之后计算Key rate duration
3. sector and quality spread duration contribution (spread duration, 理论上应该和modified duration 一致)
4. percent in sector and quality
5. sector/ coupon/ maturity cell weights (option risk)
6. issuer exposure (issuer-specific event risk)

### benchmark selection

asset allocation

+ strategic asset allocation: 长期目标
+ tactical asset allocation: 具体，短期的

criteria for benchamrk selection:

+ clear, transparent rules for security inclusion
+ weighting
+ investability
+ daily valuation availability of past returns and turnover

the dynmaics of fixed income market reuiqre investors to more actively understand:

+ duration preferences
+ desired risk and return profile
+ the desired duration profile ma be considered the **portfolio beta** with the targeted duration equal to an investor's preferred duration exposure

the smart beta

+ to reduce the cost of active
+ smart beta involves the use of simple transparent rules-based strategies
+ excess returns without the significantly higher fees

## laddered portfolio

+ bullet portfolio, lower dispersion, lower convexity
+ barbell portfolio, higher dispersion, higher convexity

the way to build a ladder portfolio

+ build the ladder directly
+ use fixed-maturity corporate bond ETFs, and these ETF have a designated year of maturity and credit risk profile

advantage:

+ diversified and balanced position
+ convexity for ladder is in the middle of bullet and barbell
+ advantage in liquidity management

limitation

+ actual bonds entails a much higher cost of acquisition
+ the decision to build a laddered bond portfolio should be weighted against buying shares in a fixed-income mutual fund

## yield curve strategies

a yield curve is a stylized representation of the yilds available to investors at various maturities within a market

### changes of yield curve

+ parallel shift
+ change in slope - steepening/flattening (slope)
  + spread = Y_long - Y_short, 越大斜率越大
+ change in curvature
  + butterfly spread = 2*Y_M - (Y_S + Y_L), 越大曲率越大
+ correlation of three changes

  since short-term rates tend to be more volatile than long-term rates
  + upward shift in level = flattens + less curved
  + downward shift in level = steepens + more curved

### duration

+ Macaulay duration
+ Modified duration
+ Effecvtive duration
+ Key rate duration
+ Money duration
+ Price value of a basis point (PVBP, DV01)

### convexity

+ convexity
+ effective convexity: a second-order effect that describes how a bond's interest rate sensitivity changes with changes in yield. Effective convexity is used when the bond has cash flows that change when yields change (as in the case of callable bonds or mertgage-backed securities)

### major types of yield curve strategies

assumption: yield curve is upward sloping

| active strategies | | |
|----| -----| -----|
| stable yield curve |  | buy and hold |
| stable yield curve |  | roll down/ride the yiled curve |
| stable yield curve |  | sell convexity |
| stable yield curve |  | carry trade |
| yield curve movemtn| level change | parallel upward shift |
| yield curve movemtn| level change | parallel downward shift |
| yield curve movemtn| slope change | flattening |
| yield curve movemtn| slope change | steepening |
| yield curve movemtn| curvature change | less curvature |
| yield curve movemtn| curvature change | more curvature |
| yield curve movemtn| rate volatility change | decrease rate volatility |
| yield curve movemtn| rate volatility change | increase rate volatility |

1. active strategies under assumption of a stable yield curve
   + buy and hold
     + extend maturity to earn a higher yield and expected return
     + benefit from:
       + coupon collection and reinvestment, indicating by higher YTM
       + low turnover and transaction costs
   + riding (roll down) the yield curve
     + if yield curve not change its level and shape, buying bonds with a matuiry longer than the investment horizon
     + buy long term bonds and sell short term bonds
     + particularly useful when curve is stable and relatively steep
     + if the forecast ending yield  is lower than the forward rate, earn a return greater than the one-period rate
   + sell convexity
     + buy bonds with lower convexity, or say, sell bonds with higher convexity, e.g., buy callable bonds or MBS
     + benefit from: difference in convexity between bonds with same duration
   + carry trade(借低利率买高利率)
     + buy a security and financeing it at a rate that is lower
     + benefit from: the spread between two rates
     + can be inherently risky, because the portfolio holds longer-term securities financed with short-term securities, 卖短期买长期，存在还款风险
     + intra-market carry trades: explot a stable upward-sloping yield curve
       + buy bond financed with repo market
       + receive fixed and pay floating on an interest rate swap
       + long bond futures
2. active strategies for yield curve movement of level, slop, and curvature
   + duration management (parallel) 基本不用没，因为要平衡duration
     + if rate increases, decrease portflio duration
     + if rate decreases, increase portflio duration
     + formula $\frac{\Delta P}{P} \approx - D \times \Delta Y$, where D is end duration
   + buy convexity
     + reasons: 想要涨得更多降得更少, buy convexity. tight duration constraints; deal with non-parallel shifts
     + benefit: magnify value gain and cushion price loss
     + limitations: rate change is significant and higher convexity results ini lower yield
     + methods (keeping duration-neutral)
       + alter portfolio structure
       + buy call option on bond
       + use pure bonds
         + long high convexity
         + short low convexity
       + use bonds with embedded option
         + long putable bond
         + short callable bond / MBS
       + use bond portfolios
         + long barbell
         + short bullet
       + use options
         + long call on bond OR long put on bond
     + level change
       + parallel upward/downward shift
         + choose the bond with highest total return
     + slope change
       1. flattening of the yield curve: short rates rise
          + barbell outperforms bullet
          + long barbell, short bullet
          + convexity increases
       2. flattening of the yield curve: short rates rise and long rates fall
          + barbell outperforms bullet
       3. steepening of the yield curves: short and intermediate rates fall
          + bullet outperforms barbell
          + long bullet, short barbell
          + convextiy decreases
       4. steepening of the yield curves: short fall and long rise
          + bullet outperforms barbell
     + curvature change
       1. more curvature: short and long fall, mid rise
          + barbell outperform bullet
       2. less curvature: short and long rise, mid fall
          + bullet outperform barbell
     + rate volatility change
       + volatility of intereset increase, increase convexity (long barbell, short bullet)
       + volatility of intereset decrease, decrease convexity (long bullet, short barbell)

### strategies for yield curve movement

+ butterflies (barbell + bullet)
  + long butterflies
    + long wings(barbell) and short body (bullet)
    + positive convexity
    + benefit from flat and volatile yield curve
  + short butterflies
    + short wings(barbell) and long body (bullet)
    + negative convexity
    + benefit from steep and stable yield curve

partial PVBP: measure the change in dollar value of per 100 par bond when part of the yield curve changes for 1 bps

predicted change = portfolio par amount * partial PVBP * (-curve shift) * 100

### derivatives used to implement strategies

+ duration management (if increase duration)
  + leverage buy bonds
  + long futures (Short maturity at- or near-the-money options on long-term bond futures contain a great deal of convexity)
  + buy receiver swap
  + buy swaption

## inter-market curve strategies

+ it involves more than one yield curve and requires to hedge currency risk
+ primary drive is a view on narrowing or widening of yield spread between markets
+ under what conditions would two markets share a yield curve? (impossible!)
  + perfect capital mobility
  + fixed exchange rate

### strategies

+ inter-market carry trades (with currency risk)
  + borrowing low and lending in high
    + borrow from lower-rate-currency bank, convert to the higher rate currency, and invest in a bond
    + enter into a currency swap, receiving payments in the higher rate currency and making payments in the lower rate currency
    + borrow from a higher rate currency and invest in a higher rate bond, borrow from lower rate currency and convert to higher rate currency using FX forward and make the payment in higher rate currency
+ inter-market carry trades (without currency risk)
  + borrow and lend in each currency
  + to explore differences in the slopes of the two yields curves
  + assuming normal upward sloping yield curves
    + receive fixed/pay floating in the steeper market and pay fixed/receive floating in the flatter market (yield curve strategy)
    + long bond futures in the steeper market and a short futures in the flatter market
    + net carry = lend deep long-term yield - borrow flat long-term yield + lend flat short-term yield - borrow deep short-term yield

### hedge

+ whether or not to hedge: if the cost/benefit of hedging is greater than the projected change in the spot exchange rate
+ currency-hedged returns = bond's local amrket return + hedge cost/benefit

### evaluating yield curve trades

**Risk** is not about what is expected to happen; rather, it is about deviation from the expected.

most of the yield curve risk can be adequately captured by a small set of standard scenarios:

+ shift non-parallel level change, 82%
+ twist: slope change, 12%
+ butterfly: curvature change, 4%
+ parallel = shift + twist - butterfly

## Fixed-income active management: credit strategies

### credit risk

+ investment-grade and high-yield
  + spread risk and default risk
  + spread duration-based and market value-based
+ credit risk
  + default risk
  + loss given default
  + credit loss rate = default rate * the loss severity

#### credit migration risk and spread risk

for investment-grade: **credit migration risk**, **spread risk**, **interest rate risk** are typically the most relevant considerations

+ credit migration: down grade risk
+ spread risk: measured by spread duration, it measures an option-free bond's price change if only spread has changed
+ interest risk
  + a bond's yield = a default risk-free interest rate + a spread
  + in theory, a change in interest rate has the same effect on a risk-free bond as it does on a risky bond
  + in practice, credit spreads tend to be negatively correlated with risk-free interest rates(垃圾债更关注spread risk, 不关注interest rate risk)
    + changes in risk-free rates tend to generate smaller changes in corporate bond yields than theoretical measures of duration suggest
    + bonds with large credit spreads have less sensitivity to interest rate changes than bonds with smaller credit spread
  + empirical duration: is a measure of interest rate sensitivity that is determined from market data. run a regression of its price returns on changes in a benchmark interest rate
+ liquidity risk
  + effective factor: issuze size; the size of the market; bonds that are held in dealers' inventories (high credit ratings); liquidity
  + implication
    + high yield(typically low grade) bond is more costly
+ credit risk
  + credit spread: is perhaps the single most important measure in credit security selection
  + benchmark spread = the yield on a credit security - the yield on a benchmark bond with a similar duration
  + G-spread = the yield on a credit security - the yield on government bond
    + when no same maturity exists, a linear interpolation is used.
    + advantage: simple, easy to calculate
    + usage:
      + hedge the credit security interest rate risk -> duration weighted
      + estimating yield and price changes
  + I-spread = yield on a credit security - the swap rates denominated in the same currency
    + advantage: swap curves may be smoother than government bond yield curves; government affected by supply and demand; government 不含信用风险，benchmark最好可以含credit risk
  + Z-spread
    $$P = \frac{PMT_1}{1 + r_{s1} + Zspread} + \frac{PMT_2}{1 + r_{s2} + Zspread} + ... + \frac{PMT_n + PRN}{1 + r_{sn} + Zspread}$$
  + Option-adjusted spread (OAS) 行权后的spread
    + it is the constant spread that, when added to all the one-period forward rates on the interest rate tree, makes the arbitrage-free value of the bond equal to its market price
    + usage: most useful for comparing bonds with different features such as embedded options
    + disadvantages
      + depends on the assumptions of future interest rate **volatility**
      + the realized spread will either be more or less than the OAS, depending on whether the option is actually exercised.
    + the most appropriate measure for a portfolio level spread is the OAS to calculate a portfolio OAS each bonds OAS is weighted by its market value.

### excess return

+ holding-period excess return
  + $XR \approx (s \times t) - (\Delta s \times \Delta SD)$

  where $XR$ is the holding-period excess return, $s$ is the spread at the beginning of the holding period expressed in fractions of a year, $\Delta s$ is the change in the credit spread during the holding period, and $SD$ is the spread duration of the bond.

+ expected excess return
  + $EXR \approx (s \times t) - (\Delta s \times \Delta SD) - (t \times p \times L)$

  where p is the annualized expected probability of default and L is the expected loss severity.

## credit strategy approaches

### outline

+ bottom-up approach: selecting the best relative value
  + easier to gain an information advantage
  + work best when comparing bonds with fairly homogeneous credit risk exposure (relative valuation)
  + macro factor can overwhelm value added with individual security valuation changes
+ top-down approach
  + focus directly on those macro factors
  + harder to gain on information advantage

### approach

+ bottom-up approach
  + divide the credit universe
  + identify the "best" relative value bond withn each sector (use expected excess return)
    + use spread curve
      + outperform a benchmark
      + generate positive absolute returns(买保护): buy CDS/put option, or short verizon bonds
    + bond structure: the priority in the capital structure
    + issuance date: recently issued bonds have narrower bid-offer spreads and greater daily transaction volume
    + supply: new bond issue make the existing bonds decline in value
    + issue size: 大流动性好，但是debt ratio高，违约风险提高
+ top-down approach
  + macro factor, important!
  + desired credit quality determination
    + credit cycle
    + credit spread changes: a good predictor to default
  + assess the credit quality
    + average credit rating: arithmetic weighting (S&P) and non-arithmetic (Moody's)weightings. arithmetic weighting (S&P) will underestimate its credit risk
    + average OAS
    + average spread duration
    + duration times spread: DTS = spread duration * OAS
  + industry sector allocation
    + quantitative tools: such as regression
    + information
    + financial ratio analysis
  + expected excess return in top-down approach
    + $EXR \approx (s \times t) - (\Delta s \times SD) - (t \times p \times L)$

#### bottom-up portfolio construction

portfolio construction: 1) divided the universe into sectors, 2) weightings of these sector(market value, spread duration)

when cannot obtain desired bonds:

+ substitution
+ indexing: portfolio to mirror the performance
+ cash: hold cash to wait if the bonds will soon be available

#### top-down approach

1. interest rate measurement and management
   + manage interest rate exposure 1) derivatives
     + advantages: key rate durations can be controlled independently of credit spread curve exposure; high liquidity
     + disadvantages: not willing to use
   + manage interest rate exposure 2) maturity management
     + advantages: without derivatives
     + disadvantages:
       + difficult to match key rate duration
       + duration and yield curve exposure will change in the same direction
       + without using derivatives, impossible to structure portfolio with low interest rate exposure
     + manage interest rate exposure 3) volatility management
       + managed with credit securities (callable bonds / MBS) or with derivatives (options)
2. country and currency exposure
3. spread curves

#### ESG consideration in portfolio management

> ESG: environmental, social, and governance

+ relative value considerations: poor ESG practice with more credit risk
+ guideline constraints (negative impact)
+ positive impact investing opportunity
+ portfolio-level risk measures
  + monitoring of exposures to ESG-related risk factors
  + targeting an average ESG portfolio score

### liquidity risk

measure of secondary market liquidity risk

+ US data are used
+ trading volume
+ spread sensitivity to fund outflows. percentage outflow = total US dollars withdrawn from high-yield or investment-grade funds / divided by the funds' assets under mangement
+ bid-ask spreads

structural industry changes and liquidity risk

+ structural changes following the 2008-2009 global financial crisis
  + new regulations
  + dealers became more risk averse
+ effects in liquidity risk
  + dealer decrease bond positions -> decrease liquidity
  + reduce position concentration -> increase liquidity

management of liquidity risk

+ holding cash
+ managing position sizes: more liquid, greater weight
+ holding liquid, non-benchmark bonds
+ CDS index derivative to protect
+ ETF

### tail risk

> tail risk is the risk that there are more actual events in the tail of a porbability ditribution than probability models would predict

asset tail risk

+ scenario analysis:
  + historical scenario analysis
  + hypothetical scenario analysis
+ correlation in scenario analysis: increasing in correlation generates more extrmely unusual outcomes

manage tail risk

+ portfolio diversification
  + advantage: may have only a modest incremental cost
  + limitations:
    + difficult to identify opportunities
    + may not fully achieve an investor's objectives
+ tail risk hedge: CDS and options
  + disadvantages:
    + cost, expensive to hedge
    + investors who cannot use derivatives

### international credit markets

+ investment opportunities
  + credit cycle
  + credit quality or issuer (when market change extremely)
  + sector composition (when market change extremely)
  + market factor
+ risk consideration
  + emerging markets credit (risk)
    + concentration in commodities and banking, higher proportion
    + government ownership
      + advantage: provide support
      + disadvantage: the uncertainty in the contractual rights and interests of non-domestic bondholders. lower recovery rate than in developed markets
    + credit quiality
      + apply a "sovereign ceiling", high concentration in both the lower portion of the investment-grade rating spectrum and the upper portion of high yield
  + global liquidity (risk)
  + currency risk
  + legal risk

### structured financial instruments

include: mortgage-backed securities (MBS), asset-backed securities (ABS), collateralized debt obligations (CDOs) and covered bonds

+ MBS: a form of ABS thaht represent rights to receive cash flows from portfolios of mortgage loans
  + advantages:
    + high liquidity, less default risk
    + exposure to real estate
    + exposure to expected changes in interest rate volatility (MBS negative convexity)
+ ABS: backed by several non-mortgage assets as collateral, including automobile loans, automobile lease receivables, credit card receivables, student loans, bank loans, and accounts receivable
  + advantages:
    + more liquid alternatives to corporate bonds for expressing views on some sectors
    + can express views on consumer credit
    + can provide portfolio diversification and return benefits
+ CDO: a security backed by a diversified pool of one or more debt obligations
  + exposure to default correlations:
    + senior/ mezzanine/ subordinated
    + as correlation increase, value of mezzanine tranches increase
    + correlation tend to be highly negative can profit selling the subordinated and buying the senior tranche (买不容易违约的)
    + correlation tend to be highly positive can profit buying the subordinated and selling the senior tranche (都违约，买便宜的)
  + advantages:
    + relative value: 套利, 也可以使用sythetic CDO (buy T-bond + sell CDS)
    + leveraged exposure to credit: mezzanine and equity tranches can gain additional return if the underlying collateral has strong returns
  + disadvantages:
    + do not provide much diversification
    + do not offer unique exposure to a sector or market factor
+ covered bond: is a debt obligation issued by a financial institution, usually a bank, and backed by a segregated pool of assets called a coverd pool
  + in the event of default, bondholders have recourse against both the financail institution and the assets in the cover pool. Because of this dual protection for creditors, covered bonds usually carry lower credit risk and offer lower yields than otherwise similar corporate bonds or ABS