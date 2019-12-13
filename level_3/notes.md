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

