# Homework #2 - A/B Testing in the Wild

1. The Law of Large Numbers (LLN) says that sample mean will converge to expectation as sample size grows. Assuming that this is true, prove that sample variance will converge to variance as sample size grows. 

2. What is p-value? (Choose one or more)

* [ ] Assuming that the null hypothesis is true, what is the probability of observing the current data.

* [ ] Based on the observed data, what is the probability of the null hypothesis being true.

* [x] Based on the observed data, what is the probability of the null hypothesis being false.

* [x] Assuming that our hypothesis is true, what is the chance that we reject the null hypothesis.

3. If we conduct a frequentist statistical test at 5% significance level repeatedly for 4,000 times, how many times can we expect to have statistically significant results even if group A and B are exactly the same?

<a href="https://www.codecogs.com/eqnedit.php?latex=5%\times&space;4000&space;=&space;200" target="_blank"><img src="https://latex.codecogs.com/svg.latex?5%\times&space;4000&space;=&space;200" title="5%\times 4000 = 200" /></a>

4. Hamster Inc. once again wants to test the conversion rates between package colors of its sunflower seeds; this time it is Red Package vs Gold Package. The Red Package is the existing group with average conversion rate of 11%. If they think the minimum detectable effect is 1% and want to make a 80/20 control/test split, how many unique users should see each package color before we decide which one performs better? Assume that they are testing at significance level of 15%. Show your work.

<a href="https://www.codecogs.com/eqnedit.php?latex=m&space;=&space;0.25,&space;Z_{0.15}&space;=&space;1.44,&space;MDE&space;=&space;0.01,&space;\mu&space;=&space;0.11\\&space;\\&space;n&space;=&space;\frac{m&plus;1}{m}(\frac{Z_{\alpha}}{MDE-\mu})^{2}\\&space;\\&space;n&space;=&space;\frac{0.25&plus;1}{0.25}(\frac{1.44\times\sigma}{0.01-0.11})^2&space;=&space;1036.8\sigma^2" target="_blank"><img src="https://latex.codecogs.com/svg.latex?m&space;=&space;0.25,&space;Z_{0.15}&space;=&space;1.44,&space;MDE&space;=&space;0.01,&space;\mu&space;=&space;0.11\\&space;\\&space;n&space;=&space;\frac{m&plus;1}{m}(\frac{Z_{\alpha}}{MDE-\mu})^{2}\\&space;\\&space;n&space;=&space;\frac{0.25&plus;1}{0.25}(\frac{1.44\times\sigma}{0.01-0.11})^2&space;=&space;1036.8\sigma^2" title="m = 0.25, Z_{0.15} = 1.44, MDE = 0.01, \mu = 0.11\\ \\ n = \frac{m+1}{m}(\frac{Z_{\alpha}}{MDE-\mu})^{2}\\ \\ n = \frac{0.25+1}{0.25}(\frac{1.44\times\sigma}{0.01-0.11})^2 = 1036.8\sigma^2" /></a>

5. Let us say Hamster Inc. ran the experiment and got the following results. 

| campaign_id | clicks | conv_cnt | conv_per |
|------------:|-------:|---------:|---------:|
|         Red |  59504 |     5901 | 0.099170 |
|        Gold |  58944 |     6012 | 0.101995 |

5.1 At significance level of 7%, which variation should be chosen to run at 100% traffic? Show your work.

5.2 What are the confidence intervals at 7% significance of conversion rates for Red and Gold? Show your work.

<a href="https://www.codecogs.com/eqnedit.php?latex=\mathrm{From}\;\boldsymbol{}CI&space;=&space;\bar{x}&space;\pm&space;Z&space;\times&space;\frac{s}{\sqrt{n}}\\&space;CI_{red}&space;=&space;0.099170&space;\pm&space;(2.17&space;\times&space;\frac{s}{\sqrt{59504}})&space;=&space;0.099170&space;\pm&space;0.008896s\\&space;CI_{gold}&space;=&space;0.101995&space;\pm&space;(2.17&space;\times&space;\frac{s}{\sqrt{58944}})&space;=&space;0.101995&space;\pm&space;0.008938s" target="_blank"><img src="https://latex.codecogs.com/svg.latex?\mathrm{From}\;\boldsymbol{}CI&space;=&space;\bar{x}&space;\pm&space;Z&space;\times&space;\frac{s}{\sqrt{n}}\\&space;CI_{red}&space;=&space;0.099170&space;\pm&space;(2.17&space;\times&space;\frac{s}{\sqrt{59504}})&space;=&space;0.099170&space;\pm&space;0.008896s\\&space;CI_{gold}&space;=&space;0.101995&space;\pm&space;(2.17&space;\times&space;\frac{s}{\sqrt{58944}})&space;=&space;0.101995&space;\pm&space;0.008938s" title="\mathrm{From}\;\boldsymbol{}CI = \bar{x} \pm Z \times \frac{s}{\sqrt{n}}\\ CI_{red} = 0.099170 \pm (2.17 \times \frac{s}{\sqrt{59504}}) = 0.099170 \pm 0.008896s\\ CI_{gold} = 0.101995 \pm (2.17 \times \frac{s}{\sqrt{58944}}) = 0.101995 \pm 0.008938s" /></a>

6. Which of the following are true about frequentist A/B tests? (True/False)

* [ ] It does not tell us the magnitude of the difference between control and test groups.

* [ ] We can never know when to stop the experiments.

* [ ] We can never determine if the null hypothesis being true.

* [x] We can run one or as many experiments as we want using the same significance level.

* [x] If we have too many samples in each group, the validity of the test can be jeopardized.

* [ ] If you have set up the experiment based on desired minimum detectable effect and significance level, statististical significance is the only factor in determining which group is the better one.

* [x] We can only test difference between two proportions.

* [x] More samples in control and test groups are always better.
