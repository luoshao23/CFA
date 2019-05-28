## Private real estate investments

## the portfolio management process and the investment policy statement

1. evaluating investor and market characteristics
2. developing an investment policy statement (IPS)
3. determing an asset allocation strategy
4. measuring and evaluating performance
5. monitoring dynamic investor objectives and capital market conditions

#### difine investment objective

+ two investment objectives
  + risk objectives

    some specific factors that affect ability to accept risk are as follows:

    + required spending needs
    + long-term wealth target
    + financail strength
    + liabilities
  + return objectives

+ five common constraints:
  + liquidity
  + time horizon
  + legal and regulatory concerns
  + tax considerations
  + unique circumstances

### an introduction to multifactor models

Arbitrage pricing theory (APT)

#### Assumptions of APT

1. unsystematic risk can be diversified away in a portfolio.
2. returns are generated using a factor model
3. no arbitrage opportuntities exist

#### the APT equation

$$E(R_P) = R_F + \beta_{P,1}(\lambda_1) + \beta_{P,2}(\lambda_2) + ... + \beta_{P,k}(\lambda_k)$$

each $\lambda$ stands for the expected risk premium; each $\beta$ represents the factor sensitivity of portfolio P to that risk factor.

#### describe and compare macroeconomic factor models, fundamental factor models, and statistical fctor models

1. macroeconomic factor models: returns are explained by surprise (or "shock") in macroeconomic risk factors (e.g., GDP, interest rate, and inflation). Factor surprises are defined as the **difference** between the realized value of the factor and its consensus predicted value.

   $$R_i = E(R_i) + b_{i1}F_{GDP} + b_{i2}F_{QS} + \epsilon_i$$

   where

   $F_{GDP}$ = surprise in the GDP rate

   $F_{QS}$ = surprise in the credit quality spread (BB-related bond yield - T bond yield)

   $b_{i1}$ = GDP surprise sensitivity of $Asset_i$

   $b_{i2}$ = credit quality spread surprise sensitivity of $Asset_i$

   `F` is a factor surprise, the difference between the predicted value of the factor and the realized value.

   `b` is the sensitivity of the stock to that surprise,

2. fundamental factor models: returns are explained by multiple firm-specific factors (e.g., P/E, market cap, leverage ratio, and earnings growth rate).
    $$R_i = a_i + b_{i1}F_{P/E} + b_{i2}F_{SIZE} + \epsilon_i$$

    where

    $F_{P/E}$ = return associted with the P/E factor

    $a_i$, the intercept term are not return surprises, nor has economical meaning

    standardized sensitivities ($b_{i1}$ and $b_{i2}$

    $$b_{i1} = \frac{(P/E)_i - \bar{P/E}}{\sigma_{P/E}}$$
3. statistical factor models use statistical methods to explain asset returns. No econmic interpretation.

#### The Macroeconomic factor model vs. the Fundamental factor model

+ sensitivites. the standard sensitivites in the fundamental factor model are calculated directly form the attribute data -- they are not estimmated. While they are regression slope estimates in macro-e factor model.
+ interpretation of factors. The macro-e factors are surprises in the macro-e variables, while the fundamental factors are rates of return associated with each factor and are estmated using multiple regression.
+ intercept term. The intercept in the macro-e factor model equals the stock's expected return, while the intercept of a fundamental factor model has no econmic interpretation.

#### the Information Ration

$$IR = \frac{\bar{R_P} - \bar{R_B}}{\sigma(R_P - R_B)}$$

where

$R_P - R_B$ = active return

$\sigma(R_P - R_B)$ = active risk = tracking error

#### Uses of multifactor models

1. passive management
2. active management
3. rules-based or algorithmic active management (alternative indices)

## Measureing and managing market risk

`Value at risk (VAR)` measures downside risk of a portfolio.

+ parametric or variance-covariance method:
  given daily mean return, $mean$ and standard deviation, $\sigma$, we have a T-day 1 - $\alpha$ confidence level in following equation:

  $$VaR_{T} = mean*T + Z_{\alpha}*\sqrt{T}\sigma$$

+ historical simulation method

+ Monte Carlo simulation

### advantages of VaR

+ simple, easy to explain
+ allow to be compared to gain a sense of relative riskiness
+ cna be used for performance evaluation
+ optimize the allocation of capital given the firm's determnination of the maximum VaR
+ acceptance of the concept VaR all over the world
+ reliability of VaR as a measure of risk can be verified by backtesting

### limitation of VaR

+ it requires many choices and can be very significant affected by these choices
+ underestimates of downside risk when fatter tails
+ liquidity often falls signigicantly when asset prices fall. A VaR which does not account for this.
+ correlations increase during periods of financail stress, which mean that VaR measures based on normal level of corrlation will overestimate diversification benefits and underestimate the magnitude of potnetial losses
+ many aspects of risk are not quantified or included
+ VaR focuses only on downside risk and extreme negative outcomes. Including consideration of right-hand tail values will give a better understanding of the risk-return trade-off.

### extensions of VaR

+ conditional VaR (CVaR) = expected tail loss or expected shortfall.
+ incremental VaR (IVaR) = the change in VaR from a change in the portfolio allocation to a security.
+ marginal VaR (MVaR) = the slope of a curve that plots VaR as a function of a security's weight in the portfolio.
+ Ex ante tracking error (relative VaR) = the VaR of the difference between the return on a portfolio and the return on its manger's benchmark portfolio.

### sensitivity risk measures and scenario risk measures

+ sensitivity analysis
+ scenario analysis
+ historical scenario
+ hypothetical scenario

$$E(R_i) = R_f + Beta_i [E(R_{MKT}) - R_f]$$

change in price = -Duration($\Delta Y$) + 1/2 Convexity $(\Delta Y)^2$

change in call price = delta($\Delta S$) + 1/2 gamma $(\Delta S)^2$ + vega($\Delta V$)

## Economics and investment markets

The value of any asset can be computed as the present value of its expected future cash flows discounted at an appropraite risk-adjusted discount rate.

Components of the discount rate are:

1. Real risk-free discount rate (R).
2. Expectedt inflation ($\pi$).
3. Risk premium reflecting the uncertainty about the cash flow (RP).

#### inter-temporal rate of substitution

inter-temporal rate of substitution = $m_t$ = marginal utility of consuming 1 unit in the future / marginal utility of current consumption of 1 unit = $\frac{u_t}{u_0}$

For a given quantity of consumption, investors prefer current consumption over future consumption ($u_0 > u_t$) and $m_t < 1$ as a result.

The current price ($P_0$) of a zero-coupon, inflation-indexed, risk-free bond that will pay $1 at time t can be expressed as:

$$P_0 = E(m_t)$$

in which case, the real risk-free rate of return is:

$$R = \frac{1 - P_0}{P_0} = \frac{1}{E(m_t)} - 1$$

#### risky cash flows and risk premiums
The investor's expected marginal utility of a payoff is inversely relted to the level of uncertainty of the pay off. This property is called as **risk-aversion**.

$P_0 = \frac{E(P_1)}{1 + R} + cov(P_1, m_1)$

#### GDP

Real interest rate is positively correlated with real GDP growth rates and volatitlitu in GDP.

For short-term risk-free securities:

$$r(short-term) = R + \pi$$

For longer term bonds, we add the risk premium for uncertainty about inflation, $\theta$

$$r(long-term) = R + \pi + \theta$$

where:

R = real risk-free rate

$\pi$ = expected inflation

$\theta$ = risk premium for uncertainty about inflation

#### Businees cycle and slope of the yield curve

recession -> low current policy rates, improving expectation about future GDP growth, increasing inflation -> higher longer-term rates -> positively sloped yield curve

A **term spread** is the difference between the yield on a longer-term bond yield and the yield on a short-term bond.

the difference between the yield of a non-inflation-indexed risk-free bond and the yield of an inflation-indexed risk-free bond of the same maturity is the **break-even inflation rate (BEI)**

$$BEI = \pi + \theta$$

#### the affect of the phase of the business cycle

Required rate of return for credit risky bonds = $R + \pi + \theta + \gamma$

where:

$\gamma$ = additional risk premium for credit risk = credit spread

#### the relationship between the consumption-hedging properties of equity and the equity risk premium

Discount rate for equity = $R + \pi + \theta + \gamma + \kappa$

where:

$\kappa$ = additional risk premium relative to risky debt for an investment in equities

#### commercial real estate

commercial real estate investments have:

+ bond-like characteristics. the steaty rental income stream
+ equity-like characteristics. value is influenced by state of the economy
+ illiquidity

discount rate for commercial real estate = $R + \pi + \theta + \gamma + \kappa + \phi$

where:

$\kappa$ = risk premium for uncertainty about terminal value of property (similar to the equity risk premium)

$\phi$ = risk premium for illquidity

## Analysis of active portfolio management

### active return

value added = active return = active portfolio return - benchmark return

$$E(R_A) = E(R_P) - E(R_B)$$

Active return is composed of two parts : asset allocation return plus security selection return:

$$E(R_A) = \sum\Delta w_i E(R_{B, i}) + \sum w_{P, i}E(R_{A, i})$$

where:

$E(R_{A, i})$ = expected active return within asset classes = $E(R_{Pi}) - E(R_{Bi})$

**Active weights** in a portfolio determin the amount value added.

**Sharp ratio (SR)** is calculated as excess return per unit of risk:

$$SR = \frac{R_P - R_F}{\sigma_P}$$

Sharp ratio is *unaffected* by the addition of cash or leverage in the portfolio.

**Information ratio (IR)** is the ratio of the active return to the standard deviation of active returns, which is known as **active risk**

$$IR = \frac{R_P - R_B}{\sigma(R_P - R_B)} = \frac{R_A}{\sigma_A} = \frac{active\ return}{active\ risk}$$

This optimal amount of active risk can be calculated as:

$$\sigma_A^* = \frac{IR}{SR_B}\sigma_B$$

The sharp ratio of a portfolio with optimal level of active risk can be calculated as:

$$SR_P = \sqrt{SR_B^2 + IR^2}$$

Furthermore, the total risk of the portfolio is given by:

$$\sigma_P^2 = \sigma_B^2 + \sigma_A^2$$

**information coefficient (IC)** is a measure of a manger's skill. IC is the ex-ante risk-weighted correlation between active returns and forecasted active returns.

$$IC = COR(\frac{R_{Ai}}{\sigma_i}, \frac{\mu_i}{\sigma_i})$$

**transfer coefficient (TC)** can be thought of as the correlation between actual active weights and optimal active weights.

$$TC = CORR(\mu_i/\sigma_i, \Delta w_i \sigma_i)$$

where:

$\mu_i$ = the ex-ante active return for security i

**Breadth** (BR) is the number of *independent* active bets taken per year. For example, if a manager takes active positions in 10 securities each month, then BR = 10 * 12 = 120.

$$BR = \frac{N}{1 + (N-1)r}$$

$$IR = (TC)IC\sqrt{BR}$$
$$E(R_A) = (TC)IC\sqrt{BR}\sigma_A$$

for an unconstrained portfolio, TC = 1

For a constrained portfolio, the optimal level of active risk ($\sigma_{CA}^*$) is calculated as:

$$\sigma_{CA}^* = TC \frac{IR^*}{SR_B}\sigma_B$$

where:

$IR^*$ = the information ratio of an unconstrained portfolio

$$SR_{PC} = \sqrt{SR_B^2 + TC^2 \times IR^{*2}}$$

for a market timer, the information coefficient is based on the proportion of correct calls:

$$IC = 2(\%correct) - 1$$