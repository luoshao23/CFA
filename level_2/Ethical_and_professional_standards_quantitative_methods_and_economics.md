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

# Economics for Valuation