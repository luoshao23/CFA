# Fixed Income

[TOC]

## Bond

+ feature: issuer, maturity, par value(redemption value), coupon rate and frequency, and currency denomination
    tenor of the bond is the time remaining until the bond's maturity date
+ legal, regulatory, tax
+ contingency provision

### Basic feature
+ issuer:
    * supranational: WB
    * sovereign governments: China
    * local governments: New York
    * quasi-governments: owned by governments
    * companies
    * special legal entities
+ maturity
+ par value
+ coupon rate and frequency
    * floating rate: example: $r_{December} = Libor_{June}(not  Libor_{Dec}!) + 25 bps$
+ currency denomination
    * dual-currency bonds: coupon in one currency and par value in another
    * currency option bonds: right to choose the currency they want to use

### Yield Measures
+ current yield
+ yield to maturity

### Legal, regulatory and tax consideration
+ trust deed or indenture
+ asset collateral backing
    * seniority ranking
        - secured bonds
            + collateral trust bonds secured by securities
            + MBS secured by mortgages
            + equipment trust certificates backed by physical assets
        - debentures: bond secured or unsecured (depend on condition)
+ credit enhancement
    * internal
        - credit tranching
        - overcollateralization
        - reserve accounts/excess spread account
    * external
        - surety bonds
        - letter of credit
+ covenants
    * affirmative covenants: `must do`
    * negative covenants: `cannot do`

#### Legal and regulatory considerations
- A domestic bond is issued by a local issuer, denominated in local currency, and sold in the domestic market. Not bearer bond.
- A Eurobond is a bond issued internationally, outside the jurisdiction of any single country. **Bearer bond(不记名)**
- A global bond issued simultaneously in the Eurobond market and in at least one domestic bond market.
- A foreign bond (Yankee bond) sold in a country and denominated in that country's currency by an entity from another country, would be registered with the SEC. Not bearer bond

### Tax consideration
The original issue discount tax provision requires the investor to include a prorated portion of the original issue discount in his taxable income every tax year until maturity.

### Structure of a bond's cash flow
+ bullet
+ fully amortized
+ partially amortized bonds

#### coupon payment structure
+ floating-rate notes: quarterly paid tied to a three month reference rate such as Libor
+ step-up bond: coupon increases by specified margins at specified dates
+ credit-linked bond: coupon changes when bond's credit rating changes
+ inverse FRN: has an inverse relationship to the reference rate.
+ capped FRN: a maximum rate is specified.


+ capital-indexed bonds - *principal*: fixed coupon rate while principal is adjusted based on changes of index
+ interest-index bonds - *coupon*: coupon linked to an index while principal is fixed at maturity
+ indexed-annuity bonds - *amortized*: fully amortized, not bullet bonds, annuity payment adjusted based on changes in an index.

### Bonds with contingency provision
+ callable bond: containing an embedded call option that gives **issuer** the right to buy the bond back from **investors** at specified prices on pre-determined dates.
    * available exercise style on callable bonds
        - American-style: continuously callable, any time starting on the first call date
        - European-style call: only once on the call date
        - Bermuda-style call: issuer has the right to call bonds on specified dates following the call protection period
+ putable bonds: it gives the **bondholder** the right to sell the bond back to the **issuer** at a pre-determined price on specified dates.
+ convertible bonds: it gives the **bondholder** the right to exchange the bond for a specified number of common shares in the **issuing company**.
    * conversion price: the price per share at which the convertible bond can be converted into shares.
    * conversion ratio: number of common shares that each bond can be converted into.
    * conversion value: conversion price * conversion ratio
    * conversion premium: convertible bond's price - conversion value
    * conversion parity: when conversion premium == 0, if conversion value of the bond is less than the bond's price, it is referred to as below parity
+ warrant: actually not an embedded option that entitles the holder to buy the underlying stock of the issuing company at a fixed exercise price until expiration date.


### Miscellaneous
+ money market security: less than 1 year; capital market: more than 1 year
+ supranational bonds repaid from the repayment of previous loans made by the issuer
+ a negative covenant protects bondholders against dilution of their claims, not to issue new debt
+ pure discount bond earns interest on an implied basis
+ covered bonds: a debt obligation backed by a segregated pool of assets called a "cover pool" from which issuer must replace non-performing assets with other performing assets
+ deferred coupon bonds: pays no coupon for their first few years but then pay higher coupons than they otherwise normally would for the remainder of their life

## Global fixed income markets
### classification
+ type of issuer
    * government and government-related sector
    * corporate sector
    * structured finance sector: securitization
+ bonds' credit quality
    * Baa3 or above by Moody's
    * BBB or above by S&P and Fitch Rating
+ maturity
    * money market: overnight to one year
    * capital market: longer than one year
+ currency denomination and type of coupon
+ where the bonds are issued and traded.

### investors in Fixed-Income securities
open market operations: refer to the purchase or sale of bonds by central bank to control monetary base.


## primary and secondary bond markets
### primary bond markets
+ public offering
    * underwritten offering(承销): investment bank guaranteed the sale of bond issue at an offering price that is negotiated with the issuer.
    * best effort offering(包销)
+ shelf registration(上架登记): 准许公司于证券公开发行的前二年即先登记，公司对于登记后在架上的股票，只要每年和每季纪录其变动状况并报告证管会即可，而公司可以选择在最有利的状况下，用最少的准备，发行股票上市。发行公司十分喜爱此种上架登记，因其交易方式具有弹性，且节省时间和费用。
+ settlement: 结算
    * corporate bonds: T+2 or T+3
    * government and quasi-government: T+1
+ auction: in many countries, most sovereign bonds are sold to the public via a public auction.

### Miscellaneous
+ The currency denomination of a bond's cash flow influences which country's interest rates affect a bond's price.
+ bonds issued by government agencies are most likely repaid first from the cash flows generated by the agency, then the national government of are backed by the taxing power

## CORPORATE DEBT
+ bilateral loan: a loan from a single lender to a single borrower
+ syndicated loan: a loan from a group of lenders to a single borrower
+ US commercial paper v.s. Eurocommercial paper

    feature|USCP|ECP
    -------|----|---
    currency|US dollar|Any
    maturity|overnight to 270 days|overnight to 364 days
    interest|discount basis(sold at par-interest, get par at maturity)|interest-bearing(sold at par, get par+interest) or discount basis
    settlement|T+0|T+2
    negotiable|can be sold to another|can be sold to another

+ serial maturity structure: a stated number of bonds mature and are paid off each year before final maturity
+ term maturity structure: paid off in one lump sum at maturityma

### Miscellaneous
Payment-in-kind: coupon bonds make periodic coupon payment, but not necessarily in cash; may pay in the form of securities

## STRUCTURED FINANCIAL INSTRUMENTS
### leveraged instrument
+ `inverse floater coupon rate = C-L*R`: C is the maximum coupon rate, L is the coupon leverage (0,1] as deleveraged while >1 as leveraged, and R is the reference rate on the reset date.


### Miscellaneous
+ repo rate: interest on a repurchase agreement
+ repo margin: difference between the market value of the security used as collateral and the value of the loan
+ OTC: buy and sell orders are initiated from various locations and then matched through a communications network. Most bonds are traded in **OTC** market.
demand deposits (also known as checking accounts) and money market accounts are retail deposits (not wholesale funds)

## BOND PRICE AND THE TIME VALUE
+ at a discount(price<par)/at a premium(price>par)
+ **lower present value will have greater percentage change of price**
+ spot rate `Zn`: yields-to-maturity `r` on zero-coupon bonds maturing at the date of each cash flow
$PV = \frac{PMT}{1+Z_1}+\frac{PMT}{(1+Z_2)^2}+...+\frac{PMT+FV}{(1+Z_N)^N} = \frac{PMT}{1+r}+\frac{PMT}{(1+r)^2}+...+\frac{PMT+FV}{(1+r)^N}$
+ day-count conventions: actual/actual;30/360
+ Flat price, accrued interest and the full price
    $$PV^{Full} = PV^{Flat} + AI$$
    $$AI = t/T * PMT$$
    $$PV^{Full} = (\frac{PMT}{1+r}+\frac{PMT}{(1+r)^2}+...+\frac{PMT+FV}{(1+r)^N})(1+r)^{t/T} = PV(1+r)^{t/T}$$

    so $PV^{Flat} = PV^{Full} - AI$
Flat prices are quoted to not misrepresent the daily increase in the full price as a result of interest accruals.

### matrix pricing
**def:** process of estimating the market discount rate and price of a bond based on the quoted or flat prices of more frequently traded comparable bonds.
    The methodology is interpolation.
### yield measures for fixed-rate bonds
$$(1+APR_m/m)^m=(APR_n/n)^n$$
- current yield: sum of the coupon payments received over the year divided by the flat price
- it is essential to compare the yields for the same periodicity to make a statement about relative value.
### yield measures for floating-rate notes
$$PV=\frac{\frac{(Index+QM)\times FV}{m}}{(1+\frac{Index+DM}{m})^1}+\frac{\frac{(Index+QM)\times FV}{m}}{(1+\frac{Index+DM}{m})^2}+...+\frac{\frac{(Index+QM)\times FV}{m}}{(1+\frac{Index+DM}{m})^N}$$
where
Index = reference rate, stated as annual percentage rate
QM = quoted margin, stated as annual percentage rate
m = periodicity of the floating-rate note, the number of payment periods per year
DM = discount margin, the required margin stated as an annual percentage rate
### yield measures for money market instruments
- pricing formula for money market instruments quoted on a discount rate basis
$$PV=FV\times (1-\frac{Days}{Year}\times DR)$$
where
Days = number of days between settlement and maturity
DR = discount rate, stated as an annual percentage rate
- pricing formula for money market instruments quoted on an add-on rate basis
$$PV = \frac{FV}{(1+\frac{Days}{Year}\times AOR)}$$
thus
$$AOR = \frac{Year}{Days}\times \frac{FV-PV}{PV}$$
where
AOR is add-on rate, stated as an annual percentage rate(also called bond equivalent yield) **year=360**

## THE MATURITY STRUCTURE OF INTEREST RATE
some possible reasons for the difference between the yields
- currency
- credit risk
- liquidity
- tax status
- periodicity

$IFR_{A,B-A}$ is a forward rate on a security that starts in period A and ends in period B. Its tenor is B-A periods. For example, `myny` means n years forward yield m years into the future.

A general formula for the relationship between the two spot rates and the implied forward rate is
$$(1+Z_A)^A\times (1+IFR_{A, B-A})^{B-A}=(1+Z_B)^B$$

- yield-to-worst: the lowest of the sequence of yield-to-call and the yield-to-maturity.
- par curve: all bonds on a par curve are assumed to have similar credit risk. Par curves are obtained from spot curves and all bonds used to derive the par curve are assumed to have the same credit risk, as well as the same periodicity, currency, liquidity, tax status and annual yields. A par curve is a sequence of yields-to-maturity such that each bond is priced at par value.
- spot curve: also known as the strip or zero curve is the yield curve constructed from a sequence of yields-to-maturities on zero-coupon bonds
- forward curve: is constructed using a series of forward rates, each having the same timeframe.
- `forward rate` can be interpreted to be the incremental or marginal return for extending the time-to-maturity of an investment for an additional time period.
- `add-on rate` (bond equivalent yield) is a rate quoted for money market instruments such as bank certificates of deposit and indices such as Libor and Euribor.
- `Yield-to-maturity` is the internal rate of return on the bond’s cash flows—the uniform interest rate such that when the bond’s future cash flows are discounted at that rate, the sum of the present values equals the price of the bond.
- An `option-adjusted spread (OAS)` on a callable bond is the Z-spread minus the value of the embedded call option expressed in basis points per year.

## Asset-Backed Security
### parties to a securitization
+ seller of the collateral, depositor
+ SPE that purchase loans or receivables and uses them as collateral to issue the ABS
+ the servicer of the loans

### structure of a securitization
subordination, also referred to as credit tranching
**SPE is bankruptcy remote from corporate**

## RESIDENTIAL MORTGAGE LOANS
### interest rate determination
+ fixed rate
+ adjustable or variable rate: mortgage rate is reset periodically
+ initial period fixed rate: mortgage rate is fixed for some initial period and is then adjusted.
+ convertible: the mortgage rate is initially either a fixed rate or an adjustable rate.

+ recourse loan: 有追索权贷款
+ non-recourse loan: 无追索权贷款

+ interest-only mortgage: there is no scheduled principal repayment for a certain number of years, in extreme case, interest-only lifetime mortgage or bullet mortgage

## RESIDENTIAL MORTGAGE-BACKED SECURITIES (RMBS)
exposed to prepayment risk
1. securities backed by federal agencies
2. GSE Government sponsored enterprises
3. issued by private entities

+ agency RMBS: 1 & 2
+ non-agency RMBS: 3

### mortgage pass-through security
+ pass-through rate
+ WAC: weighted average coupon rate
+ WAM: weighted average maturity
+ PSA: Public securities association prepayment benchmark. For example, 80PSA means the prepayment rate of the mortgage to be 80% monthly prepayment rates forecasted by the PSA model.
+ SMM: single monthly mortality
$$SMM=\frac{prepayment\ for\ the\ month}{beginning\ outstanding\ mortgage\ balance\ for\ the\ month - scheduled\ principal\ repayment\ for\ the\ month}$$

+ interest rate declines -> prepayment rate goes up-> contraction risk(receive payments faster than anticipated)
+ interest rate rise -> prepayment rate lower -> extension risk(receive payments slower than anticipated)

### Collateralized mortgage obligation (CMO)
meets the asset/liability requirements of institutional investors
+ Sequential pay CMO
+ PAC: planned amortization class tranches
+ non-PAC: support tranches

## COMMERCIAL MORTGAGE-BACKED SECURITY (CMBS)
### credit risk
+ loan-to-value ratio(LTV)
+ debt-service-coverage ratio (DSC): equal to the property's annual net operating income(NOI) divided by the debt service. A DSC ration that exceeds 1.0 indicates that the cash flows from the property are sufficient to cover the debt service while maintaining the property in its initial state of repair.

## NON-MORTGAGE ASSET-BACKED SECURITIES
### auto loan ABS
loss compensation order
reserve account + overcollateralization -> privately placed notes -> subordinated -> senior
### credit card receivable ABS

auto loan ABS| credit card loan receivable ABS
-------------|------
amortizing loans|non-amortizing loans

### CMBS structure
+ call protection(protects investors against prepayment risk)
    at loan level
    * prepayment lockout
    * prepayment penalty points
    * yield maintenance charge
    * defeasance
+ subordination improves the credit rating of the CMBS

## COLLATERALIZED DEBT OBLIGATIONS (CDO)
+ CBO: CDO backed by corporate and emerging market bonds
+ CLO: CDO backed by leveraged bank loans
+ structured finance CDO: CDO backed by ABS, RMBS, CMBS and other CDOs
+ synthetic CDO: CDO backed by a portfolio of credit default swaps for other structured securities

### Miscellaneous
the monthly cash flows of a mortgage pass-through security depend on the cash flows of the underlying pool of mortgage, but their amount and timing cannot be known with certainty because of payments.

- tranching: time tranching(different maturity); credit tranching(different credit risk level)
- CPR: an annualized rate, which indicates the percentage of the outstanding mortgage pool balance at the beginning of the year that is expected to be prepaid by the end of the year.

## Fixed-income risk and return
### source of return
+ receipt of the promised coupon and principal payments on the scheduled dates
+ reinvestment of coupon payments
+ potential capital gains or losses on the sale of the bond **prior to maturity**

+ horizon yield: the internal rate of return between the total return and the purchase price of the bond. annualized holding-period rate of return.

+ two types of interest rate risk on a fixed-rate bond: **coupon reinvestment risk** and **market price risk**.
    - coupon reinvestment risk increases with a higher coupon rate and a longer reinvestment time period.
    - market price risk dominates coupon reinvestment risk when the investor has a short-term horizon
    - coupon reinvestment risk dominates market risk when the investor has a long-term horizon

### yield volatility
Longer-term bond yields are mostly determined by future inflation and economic growth expectations. Those expectations often tend to be less volatile.

### maclauly, modified, and approximate duration
Macaulay duration is the weighted average of the time to receipt of coupon interest and principal payments, in which weights are the shares of the full price corresponding to each payment.

$$MacDur = \left[\frac{\frac{(1-t/T)\times PMT}{(1+r)^{1-t/T}}+\frac{(2-t/T)\times PMT}{(1+r)^{2-t/T}}+...+\frac{(N-t/T)\times PMT}{(1+r)^{N-t/T}}}{\frac{PMT}{(1+r)^{1-t/T}}+\frac{PMT+FV}{(1+r)^{2-t/T}}+...+\frac{PMT+FV}{(1+r)^{N-t/T}}}\right]$$
where
t = the number of days from the last coupon payment to the settlement date
T = the number of days in the coupon period
r = the yield-to -maturity, or the market discount rate, per period
or

$$MacDur = \left\\{ \frac{1+r}{r}-\frac{1+r+[N\times (c-r)]}{c\times [(1+r)^N-1]+r}  \right\\} -(t/T)$$

$$ModDur=\frac{MacDur}{1+r}$$
ModDur provides an estimate of the percentage price change for a bond given a change in its yield-to-maturity.

Macaulay and modified durations are inversely related to the coupon rate and the yield-to-maturity.

$$\%\Delta PV^{Full}\approx -AnnModDur \times \Delta Yield$$
for example, annual yield 6% semmiannual payment bond jumps by 100 bps, from 6.00% to 7.00%, the estimated loss in value for the bond is 6.1268%

$$\%\Delta PV^{Full}\approx -6.126829 \times 0.0100 = -0.061268$$

$$AppoxModDur = \frac{(PV_{-})-(PV_{+})}{2 \times (\Delta Yield) \times (PV_0)}$$

$$ApproxMacDur = ApproxModDur \times (1+r)$$

### effective duration
Another way is to estimate the percentage change in price given a change in a **benchmark yield curve**--for example, the government par curve.
$$EffDur = \frac{(PV_{-})-(PV_{+})}{2 \times (\Delta Curve) \times (PV_0)}$$

### key rate duration(partial duration)
it is a measure of a bond's sensitivity to a change in the benchmark yield curve at a specific maturity segment.

### money duration of a bond and the price value of a basis point

$$MoneyDur = AnnModDur \times PV^{Full}$$

$$\Delta PV^{Full} \approx -MoneyDur \times \Delta Yield$$

$$PVBP = \frac{(PV_{-}) - (PV_{+})}{2}$$

$PV_{-}$ and $PV_{+}$ are the **full prices** calculated by decreasing and increasing the yield-to-maturity by **1 bp**.

$$\%\Delta PV^{Full} \approx -MoneyDur \times \Delta Yield + [1/2 \times AnnConvexity \times (\Delta Yield)^2]$$

$$ApproxCon = \frac{(PV_{-}) - (PV_{+}) - [2\times (PV_0)]}{(\Delta Yield)^2 \times (PV_0)}$$

+ the duration gap is a bond's Macaulay duration minus the investment horizon.

## credit risk
Credit risk is the risk of loss resulting from the borrower failing to make full and timely payments of interest and/or principal.

+ default risk: or default probability
+ loss severity: equals (1 - recovery rate)

best measure of credit risk:
$$Expectated\ loss = Default\ probablity \times Loss\ severity\ given\ default$$

> credit related risk:
+ **spread risk**: a yield premium to bonds that have been considered "default-risk free"
+ **credit migration risk or downgrade risk**: bond issuer's creditworthiness deteriorates
+ **market liquidity risk**

### seniority ranking
+ secured debt
+ unsecured debt

### priority of claims
First lien loan-senior secured -> second lien loan-secured -> senior unsecured -> senior subordinated -> subordinated -> junior subordinated
Not always absolute:

+ with a secured claim have the right to the value of that specific property
+ unsecured creditors have a right to be paid in full before holders of equity interests
+ senior unsecured creditors take priority over all subordinated creditors

### Credit rating
three major global credit rating agencies--Moody's, S&P, and Fitch

#### Investment grade

Moody's|S&P|Fitch
-------|----|-----
Aaa ~ Baa3|AAA ~ BBB-|AAA ~ BBB-


+ credit ratings can change over time
+ credit ratings tend to lag the market's pricing of credit risk
+ ratings agencies may make mistakes
+ some risks are difficult to capture in credit rating, including litigation risk, environmental and business risks

#### issuer v.s. issue ratings
an issuer credit rating is meant to address an obligor's overall creditworthiness; issue rating refer to specific financial obligations of an issuer and take into consideration such factors as ranking in the capital structure.
`notching`

`structural subordination` can arise when a corporation with a holding company structure has debt at both its parent holding company and operating subsidiaries.
+ issuer credit rating usually applies to its **senior unsecured debt**.

## credit analysis v.s. equity analysis

### four Cs of credit analysis
+ `capacity`: ability of the borrower to make its debt payments on time; **focus**
    * industry structure
        - threat of entry
        - power of suppliers
        - power of buyers/customers
        - threats of substitute
        - rivalry among existing competitors
    * industry fundamentals
        - cyclical or non-cyclical
        - growth prospects
        - published industry statistics
    * company fundamentals
        - competitive position
        - track record/operating history
        - management's strategy and execution
        - ratios and ratio analysis
            + profitability and cash flow
                * EBIT, EBITDA, funds from operations (FFO), Free cash flow before/after dividend (FCF before/after dividends)
            + leverage
                * Debt/capital, Debt/EBITDA, FFO/debt, FCF after dividends/debt
            + coverage
                * EBITDA/interest expense, EBIT/interest expense

                > EBITDA = operating income + DA

    * comments on issuer liquidity
        - cash on the balance sheet
        - net working capital
        - operating cash flow
        - committed bank lines
        - debt coming due and committed capital expenditures in the next one to two year

> 资产Asset是一个公司所控制的可以产生经济效益的资源
> 资本Capital是投资人往公司投入的资源，投资人包括债权人和股权人
> 资产(Asset) = 固定资产(Fixed Asset) + 流动资产(Curent Asset) = 债券投资(Debt) + 股东权益(Equity) + 其他债务(Other Liability)
> 资本(Invested Capital) = 固定资产(Fixed Asset) + 净运营资本(Net Working Capital) = 债权投资(Debt) + 股东权益(Equity)
> 通过capital购买asset,从而产生未来经济效益

+ `collateral`: quality and value of the assets supporting the issuer's indebtedness
+ `covenants`: terms and conditions of lending agreements that the issuer must comply with
    * obligation to do
    * limited in doing
    For corporate bonds, it is described in the bond `prospectus`.

    key covenants for high-yield issuers may include the following:
    * change of control put: bondholders have right to require issuer to buy back their debt when acquired
    * restricted payments: protect creditors by limiting how much cash can be paid out to shareholders over time.
    * limitations on liens: put limits on how much secured debt an issuer can have
    * restricted versus unrestricted subsidiaries
+ `character`: quality of the management

## credit risk v.s. return yields and spreads

Yield corporate bond = real risk-free interest rate + expected inflation rate + maturity premium + liquidity premium + credit spread

Yield spread = liquidity premium + credit spread

Spread can be affected by these factors：
+ credit cycle
+ broader economic condition
+ financial market performance overall including equities
+ broker-dealers' willingness to provide sufficient capital for market making
+ general market supply and demand

$$Price\ impact \approx -ModDur \times \Delta Spread$$

for larger spread changes, the impact of convexity needs to be incorporated into the approximation:

$$Price\ impact \approx -(ModDur \times \Delta Spread) + 1/2C_{vx} \times (\Delta Spread)^2$$




