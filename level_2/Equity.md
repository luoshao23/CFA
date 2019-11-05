## Equity valuation: application and processes

The general steps in the equity valuation process are:

1. Understand the business
2. Forecast company performance
3. Select the appropriate valuation model
4. Convert the forecasts into a valuation
5. Apply the valuation conclusions

$$IV_{analyst}  - price = (IV_{actual} - price) + (IV_{analyst} - IV_{actual})$$

**going concern assumption** = a company will continue to operate as a business, as opposed to going out of business.

### Elements of industry structure

1. Threat of new entrants in the industry
2. Threat of substitutes
3. Bargaining power of buyers
4. Bargaining power of suppliers
5. Rivalry among existing competitors

## Return concepts

### Holding period return

holding period return = r = $\frac{P_1 - P_0 + CF_1}{P_0}$

+ realized holding period return
+ expected holding period return

### calculate an equity risk premium

equity risk premium = required return on equity index - risk-free rate

required return for stock j = risk-free return + $\beta_j$ * (equity risk premium)

#### estimates of the equity risk premium

+ Historical estimates: survivorship bias
+ forward-looking estimates
  + Gordon growth model

    $$(D_1 / P) + \hat{g} - r_{LT, 0}$$
  + Supply-side estimates (Macroeconomic models)

    equity risk premium = $(1+i)\times(1+r_{EPS})\times(1+g_{P/E}) - 1 + Y - r_f$

    where:

    i = expected inflation

    r_{EPS} = expected real growth in EPS

    g_{P/E} = expected changes in the P/E ratio

    Y = the expected yield on the index

    r_f = the expected risk-free rate

  + survey estimates
  + CAPM

    required return on stock j = risk-free rate + (equity risk premium * beta of j)

  + multifactor models

    required return = RF + (risk premium)_1 + (risk premium)_2 + ... + (risk premium)_n

    (risk premium)_i = (factor sensitivity)_i * (factor risk premium)_i

    + Fama-French model

        required return of stock j = $RF + \beta_{mkt, j} \times (R_{mkt} - RF) + \beta_{SMB, j} \times (R_{small} - R_{big}) + \beta_{HML, j} \times (R_{HBM} - R_{LBM})$

        where:

        (R_{mkt} - RF) = return on a value-weighted market index minus the risk-free rate

        $(R_{small} - R_{big})$ = a small-cap return premium

        $(R_{HBM} - R_{LBM})$ = a value return premium

    + Pastor-Stambaugh model = Fama-French model + liquidity factor
    + Macroeconomic multifactor models
        1. confidence risk
        2. time horizon risk
        3. inflation risk
        4. business cycle risk
        5. market timing risk
    + Build-up method
        required return = RF + equity risk premium + size premium +specific-company premium
    + Bond-yield plus risk premium method

### Beta estimates

#### Adjusted beta for public companies

adjusted beta = (2/3 * regression beta) + (1/3 * 1.0)

#### Beta estimates for thinly traded stocks and nonpublic companies

1. identify a benchmark company, XYZ,  which is publicly traded and similar to ABC in its operations
2. unlever the beta for XYZ:

    unlevered beta for XYZ = (beta of XYZ) / (1 + D/E of XYZ)

3. lever up the unlevered beta for XYZ to get an estimate of ABC's beta

    estimate of beta for ABC = (unlevered beta of XYZ) * (1 + D/E of ABC)

## Industry and company analysis

### equity valuation method

+ bottom-up: starts with analysis of an individual company
+ top-down: begins with expectations about a macroeconomic vairbale, ofthen the growth rate of nominal GDP.
+ hybrid

### forecast the following costs:

forecast COGS = (1 - gross margin)(estimate of future revenue)

#### income tax expense

1. statutory rate
2. effective tax rate
3. cash tax rate

## Discounted dividend valuation

The fundamental value represents not only the present value of the future dividends (on a non-growth basis) but also the present value of the growth opportunites (PVGO):

$$V_0 = \frac{E_1}{r} + PVGO$$

### P/E ratios

justified leading P/E = $\frac{P_0}{E_1} = \frac{1 - b}{r - g}$

justified trailing P/E = $\frac{P_0}{E_0} = \frac{(1 - b) \times (1 + g)}{r - g}$

### H-Model

$$V_0 = \frac{D_0 \times (1 + g_L)}{r - g_L} + \frac{D_0 \times H \times (g_S - g_L)}{r - g_L}$$

### sustainable growth rate (SGR) using DuPont analysis

$$SGR = b \times ROE$$

where:

b = earning retention rate = 1 - divident payout rate

g = ((net income - dividends) / net income) * (net income / sales) * (sales / total assets) * (total assets / equity) = R * P * A * T

### FCFF and FCFE

FCFF = Cash revenue - WCInv -FCInv - Cash operating expense

FCFE = FCFF - Interest payment + net borrowing

firm value = FCFF discounted at the WACC

equtiy value = FCFE discounted at the required return on equity

equity value = firm value - market value of debt

FCFF = NI + NCC + [Int * (1 - tax rate)] - FCInv - WCInv

where:

NCC = noncash charges

FCInv = capital expenditures - proceeds from sales of long-term assets

(Almost) FCFF = (NI + NCC - WCInv) - FCInv = CFO - FCInv

(Actual) FCFF = (NI + NCC - WCInv) + Int(1 - tax rate) - FCInv = CFO Int(1 - tax rate) - FCInv

FCFF = EBIT(1 - tax rate) + Dep - FCINv - WCInv

FCFF = EBITDA(1 - tax rate) + tax rate * Dep - FCInv - WCInv

FCFE = NI + NCC - FCInv - WCInv + net borrowing

For forecasting FCFE, use:

FCFE = NI [(1 - DR) * (FCInv - Dep)] - [(1 - DR) * WCInv]

value of the firm = $\frac{FCFF_1}{WACC - g} = \frac{FCFF_0 \times (1+g)}{WACC - g}$

value of equity = $\frac{FCFE_1}{WACC - g} = \frac{FCFE_0 \times (1+g)}{WACC - g}$

PEG ratio = $\frac{P/E ratio}{g}$

EV = market value of common stock + market value of preferred equity + market value of debt + minority interest - cash and investments

earings surprise = reported EPS - expected EPS

SUE = earnings surprise / standard deviation of earings surprise

## Residual income valuation

EVA (Economic value added) = NOPAT - (WACC * capital) = EBIT(1 - t) - $WACC

MVA (Market value added) = market value - total capital

$$RI_t = E_t - (r \times B_{t-1}) = (ROE - r) \times B_{t-1}$$

### Discount for lack of control

DLOC = 1 - 1 / (1 + control premium)

total discount = 1 - [(1 - DLOC)(1 - DLOM)]

where:

DLOM = discount for lack of mmarketability

## REITS

NAV = Value of operating real estate + value of other tangible assets - value of liabilities

FFO = net earnings + depreciation + deferred tax charges +/- Losses/gains from sales of property and debt restructuring

AFFO = FFO - non cash rent - maintenance-type capital expenditutrd and leasing costs
