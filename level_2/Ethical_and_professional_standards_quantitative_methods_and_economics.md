# Ethical and Professional Standards

**The standard of professional conduct**
1. Professionalism

    + knowledge of the law: comply with the more strict law
    + independence and objectivity: must not offer, solicit or accept any gift, benefit and so on
    + misrepresentation(曲解误报): must not knowingly make any misrepresentations
    + misconduct: must not engage in any ptofessional conduct involving dishonesty...

2. Integrity(正直) of capital markets

    + material nonpublic information: must not act or cause others to act on the information
    + market manipulation

3. Duties to Clients

    + loyalty, prudence(审慎) and care: must act for the benefit of their clients and place their clients' interests before their employer's or their own interests
    + fair dealing
    + suitability
        - make a reasonabel inquiry prior to making any investment recommendation
        - determine that an investment is consistent with the clients' written objectives and constraints
        - judge the suitability of investments in the context of the client's total portfolio
    + preformance presentation
    + preservation of confidentiality: **MUST** keep information abount current, former and prospective clients confidential **unless**:
        - the information concerns illegal activities
        - disclosure is required by law, or
        - the client permits disclosure of the information

4. Duties to Employers

    + loyalty: in matters related to employment, must act for the benefit of their employer and not cause harm to them
    + additional compensation arrangements: must not accept benefits with or might reasonabley be expected to create a conflict of interest with emloyer's unless obtain written consent from all parties involved.
    + responsibilities of supervisors

5. Investment analysis, recommendations, and actions

    + diligence and reasonable basis
    + communication with clients and prospective clients
        - must disclose format and principles and promptly disclose any changes
        - disclose significant limitations and risks
        - identify important factors to their investment and include factors in communication with clients and prospective clients
        - distinguish between fact and opinion
    + record retention

6. Conflicts of interest

    + disclosure of conflicts: make sure the disclosure are prominent, are delivered in plain language
    + priority of transactions
    + referral fees(介绍费): must disclose to emloyers, clients and prospective clients any compensation received by, or paid to, others for the recommendation of products or service

7. Responsibilities as a CFA Institute Menber or CFA Candidate

    + conduct as participants in CFA Institute Programs: must not engage in any conduct that compromises the reputation of CFA
    + reference to CFA: must not misrepresent or exaggerate the meaning

# Ethical and Professional Standards: Application
# Quantitative Methods for Valuation

`significance level` like 5%

`confidence level` like 95%, i.e. (1 - significance level)
## correlation and regression
`sample covariance`
$$cov_{XY} = \frac{\sum_{i=1}^n(X_i-\bar{X})(Y_i-\bar{Y})}{n - 1}$$

`sample correlation coefficient`
$$r_{XY} = \frac{cov_{XY}}{(s_X)(s_Y)}$$

| correlation coefficient | Interpretation               |
| ----------------------- | ---------------------------- |
| $r= +1$                 | perfect positive correlation |
| $0 < r < +1$            | positive linear relationship |
| $r = 0$                 | no linear relationship       |
| $-1 < r < 0$            | negative linear relationship |
| $r= -1$                 | perfect negative correlation |

### test of hypothesis

To test whether the correlation between the population of two variable is equal to zero
$$H_0: \rho = 0 \ versus\ H_a:\rho \ne 0$$

we can use a t-test to determine wether the null hypothesis should be rejected with $df=n-2$ :

$$t = \frac{r\sqrt{n-2}}{\sqrt{1-r^2}}$$

Reject $H_0$ if $+t_{critical} < t$, or $t < - t_{critical}$

### simile linear regression model
The estimated slope coefficient for the regression line describes the change in Y for a one unit change in X. And it is calculated as:

$$\hat{b_1} = \frac{cov_{XY}}{\sigma^2_X}$$

the intercept term ($\hat{b_0}$) may be expressed as:

$$\hat{b_0} = \bar{Y} - \hat{b_1}\bar{X}$$

### standard error of estimate (SEE) and coefficient of determination ($R^2$)

The confidence interval for the regression coefficient, $b_1$ is calculated as:
$$\hat{b_1} \pm (t_c \times s_{\hat{b_1}})$$
Where, $t_c$ is the critical two-tailed t-value for the selected confidence level with the appropriate number of degrees of freedom, which is equal to the number of sample observation minus 2.

A t-test may also be used to test the hypothesis that the true slope coefficient $b_1$ is equal to some hypothesized value. Letting $\hat{b_1}$ be the point estimate for $b_1$, the appropriate test static with n-2 degrees of freedom is:

$$t_{b_1} = \frac{\hat{b_1} - b_1}{s_{\hat{b_1}}}$$

Reject $H_0$ if $t >  + t_{critical}$ or $t <  - t_{critical}$

### confidence intervals for predicted values

The equation for the confidence interval for a predicted value of Y is:

$$\hat{Y} \pm (t_c \times s_{f})$$
where:

$t_c$ = two-tailed critical t-value at the desired level of significant with df = n - 2

$s_f$ = standard error of the forecast

If you do need to calculate $s_f$, it can be done with the following formula:
$$s_f^2 = SEE^2(1+\frac{1}{n} + \frac{(X-\bar{X})^2}{(n-1)s_x^2})$$

### ANOVA
+ Total sum of squares (SST)
$$SST = \sum_{i=1}^n (Y_i - \bar{Y})^2$$
+ Regression sum of squares (RSS)
$$RSS = \sum_{i=1}^n (\hat{Y_i} - \bar{Y})^2$$
+ Sum of squared errors (SSE)
$$SSE = \sum_{i=1}^n (Y_i - \hat{Y_i})^2$$

Thus, total variation = explained variation + unexplained variation, or:

SST = RSS + SSE

| Source of variation    | Degrees fo Freedom | Sum of Squares | Mean Sum of Squares                         |
| ---------------------- | ------------------ | -------------- | ------------------------------------------- |
| Regression (explained) | 1                  | RSS            | $MSR = \frac{RSS}{k} = \frac{RSS}{1} = RSS$ |
| Error (unexplained)    | n - 2              | SSE            | $MSE = \frac{SSE}{n-2}$                     |
| Total                  | n - 1              | SST            |                                             |

k is the number of slope parameters estimated and n is the number of observation. In general, the regression $df = k$ and the error $df = (n-k-1)$. So in one independent variable linear regression, we use $k=1$ for regression and $n-1-1=n-2$ for the error.

### Calculating $R^2$ and SEE

$$R^2 = \frac{SST - SSE}{SST} = \frac{RSS}{SST}$$

The SEE is the standard deviation of the regression error terms and is equal to the square root of the mean squared error (MSE):

$$SEE = \sqrt{MSE} = \sqrt{\frac{SSE}{n-2}}$$

### The F-statistic

$$F = \frac{MSR}{MSE} = \frac{RSS/k}{SSE/(n-k-1)}$$
**IMPORTANT:** This is always a one-tailed test!

In fact, in simple linear regression we have $t^2 = F$, see [Relationship between F and t statistics](http://www-ist.massey.ac.nz/dstirlin/CAST/CAST/HsimpleAnova/simpleAnova3.html)

## Multiple regression and issues in regression analysis

### Hypothesis testing of regression coefficients
The t-statistic used to test the significance of the individual coefficients in a multiple regression is calculated using the same formula that is used with simple linear regression.
$$t = \frac{\hat{b_j} - b_j}{s_{\hat{b_j}}} = \frac{estimated\ regression\ coefficient - hypothesized\ value}{cofficient\ standard\ error\ of\ b_j}$$

### Interpreting p-Values
The `p-value` or probability value or asymptotic significance is the probability for a given statistical model that, when the null hypothesis is true, the statistical summary (such as the sample mean difference between two compared groups) would be **the same as or of greater** magnitude than the actual observed results.:

+ If the p-value is less than significance level, the null hypothesis can be rejected.
+ If the p-value is greater than the significance level, the null hypothesis cannot be

### F statistic

The *F-statistic*, whihc is always a one-tailed test, is calulated as:

$$F = \frac{MSR}{MSE} = \frac{RSS/k}{SSE/(n-k-1)}$$
where:

$RSS$ = regression sum of squares

$SSE$ = sum of squared errors

$MSR$ = mean regression sum of squares

$MSE$ = mean squared errors

### Coefficient of determination, $R^2$
$R^2$ is also calculated the same way as in simple linear regression.
$$R^2 = \frac{SST - SSE}{SST} = \frac{RSS}{SST}$$
#### Adjusted $R^2$
Unfortunately, $R^2$ by itself may not be a reliable measure of the explanatory pwoer of the multiple regression model. This is because $R^2$ **almost always increases as variables are added to the model**, even if the marginal contribution of the new variable is not statistically significant. The adjusted $R^2$ value is expressed as:
$$R_a^2 = 1 - [(\frac{n-1}{n-k-1})\times(1-R^2)]$$

### ANOVA Tables

| Source     | df (Degrees fo Freedom) | SS (Sum of Squares) | MS (Mean Sum of Squares)                    |
| ---------- | ----------------------- | ------------------- | ------------------------------------------- |
| Regression | k                       | RSS                 | $MSR = \frac{RSS}{k}$ |
| Error      | n - k - 1               | SSE                 | $MSE = \frac{SSE}{n-k-1}$                   |
| Total      | n - 1                   | SST                 |                                             |
### What is heteroskedasticity?
`Heteroskedasticity` occurs when the variance of the residual is not the same across all observations in the sample.

#### Effect of heteroskedasticity on regression analysis
There are four effects of heteroskedasticity you need to be aware of:
+ The stanard errors are usually unreliable estimates.
+ The coefficient estimates (the $\hat{b_j}$) aren't affected.
+ If the standard errors are too small, but the coefficient estimates themselves are not affected, the t-statistics will be too large and the null hypothesis of no statistical significance is rejected too often, The opposite will be true if the standard errors are too large.
+ The F-test is also reliable.

### Detecting heteroskedasticity
There are two methods to detect heteroskedasticity: examing scatter plots of the residuals and using the Breusch-Pagan chi-square ($\chi^2$) test.

The BP chi-square test, which has a chi-square ($\chi^2$) distribution, is calculated as:

BP chi-square test = $n \times R_{resid}^2$ with k degrees of freedom

where:

n = the number of observations

$R_{resid}^2$ = $R^2$ from a second regression of the squared residuals from the first regression on the independent variables

k = the number of the independent variables

### Correcting heteroskedasticity
The most common remedy and the one recommended in the CFA exam is to calculate *robust standard errors* (also called White-corrected standard errors or heteroskedasticity-consistent standard errors). The second is to correct for heteroskedasticity is the use of *generalized least squares*.

$$t = \frac{Coefficient}{White-corrected\ standard\ errors}$$
# Economics for Valuation