# Final Project: Design an A/B test

## Experiment Design

### Metric Choice
The invariant metrics I used are: Number of cookies, Number of clicks.

The evaluation metrics I used are: Gross conversion, Retention, and Net conversion.

For each metric:

Number of cookies: I chose it as invariant metric because when users browse the webpage, he/she already has one unique browser id. Thus it is independent and it will be consistent in this experiment. In the meanwhile, an invariant metric cannot both be an evaluation metric because: Invariant metric is the one that won't be affected by the experiment. However, evaluation metric is the one dependent on the experiment design.

Number of user-ids: user-ids are people who enrolled the course. Thus it will be affected by the experiment between the experiment and control groups. It is not chosen as evaluation metric because it is a count, instead of a percentage which can be further normalized or standardized.

Number of clicks: I chose it as invariant metric because people need to click, then he/she can see the content/experiment. Thus it is independent from the experiment.

Click-through-probability: It could be a good invariant metric but I didn't choose it because I personally think the number of cookies and number of clicks are highly correlated with the click-through-probability.

Gross conversion: I choose it as evaluation metric because user-ids are dependent on the effect of the experiment. And in the alternative hypothesis, we expect to see lower value in the experiment gorup, because we hypothesize that people without enough time per week will not enroll the course.

Retention: This value can be a candidate of evaluation metric because it dependents on the experiment. This value is expected to be higher in the experiment group because people need to have more time commitment per week to enroll in the course, and thus make their first payment. But I feel it is similiar to Net conversion, and it is highly correlated with Net conversion, we can even calculated it using Net conversion and number of user-ids and cookies. I didn't end up choosing it as the value.

Net conversion: I chose it as evaluation metric because it is affected by the experiment. In the experiment group, since most people can commit enough hours per week, and are more toward stay (make the first payment). So, this value should be increased, or at least not decreased.


### Measuring Standard Deviation
Goss conversion: 0.0202

Net conversion: 0.0156

Gross conversion, and net conversion are percentages, they are using the number of cookies as their denomiators. I treat them as unit of diversion. And analytical estimate is comparable to the empirical variation.

### Sizing
#### Number of sample vs. power

I did not use the Bonferroni correction. And I used Gross conversion, and Net conversion as evaluation metrics.
I would need 685325 pageviews for a test of alpha = 0.05 and beta = 0.2.

#### Duration vs. Exposure

I chose to set 0.8 (80%) as the number of fraction to be exposed. Since 80% will be exposed and the subsequent impact will be minimum. It will not bring too much potential harm to Udacity's business. Furthermore, the experiment itself is not too risky because it will only be a popup message. Nothing too sensative (it does not collect users' private infomation nor any sensative information).

For the duration, since I need 685325 page views in total, and 40000 people, with 80%, roughly 22 days will yield the desired results.

## Experiment Analysis
### Sanity Checks

No Bonferroni correction

Number of cookies: Lower bound - 0.4988, Upper bound - 0.5011, Observed - 0.5006. It passes the Sanity Checks.

Number of clicks: Lower bound - 0.4959, Upper bound - 0.5041, Observed - 0.5005. It passes.

### Result Analysis
#### Effect Size Tests

No Bonferroni correction

Gross conversion: Lower bound - -0.0291, Upper bound - -0.0120. It is statistical significance and practical significance.

Net conversion: Lower bound - -0.0116, Upper bound - 0.0019, It is not statistical significance. It is not practical significance.

#### Sign Tests

No Bonferroni correction

Gross conversion: p-value - 0.0026. It is statistical significant 

Net conversion: p-value - 0.6776. It is not significant.

#### Summary

I didn't use Bonferroni correction. Besides all of our metrics must launch criteria, Bonferroni correction is not a good fit for this experiment.

If we use more number of metrics, we are more likely to make type I error (falsely reject the null hypothesis when the null is true. So by introducing the Bonferroni correction, we can reduce this error by reducing alpha. 

However, if we reduce the type I error, we are increasing the Type II error -- accepting null, when null is false. Because of our experiment, we don't want to increase Type II error. So I didn't use Bonferroni correction.

From the result: significant in Gross conversion, but insignificant in Net conversion, it means that the popup message did have impact on the students' decision to register the courses, but it didn't end up having to much students enrolled to make their payment for the course.

### Recommendation

Since Net conversion has 0 in the confidence interval, it is not significant. And it contains negative values, it might cause some warry regarding carry this experiment. However, we can redesign some other factors before experiment.

Simply based on this experiment, I wouldn't recommend the new feature. For the Gross conversion, only people who are willing to commit more time per week are more toward paying for the courses. This experiment could cause less students to view the free courses. From Net conversion, the new feature doesn't attract more students to pay after their free courses. Besides, the negative values in the confidence intervals might be a potential concern for Udacity's profit. Since we want students be more clearer what the program requires: need at least 5 hours per week, we don't want to frustrate students by having them find out too much burden after enrolling. Thus, Udacity has less cancellation.

## Follow-Up Experiment

Udacity's charging policy is a potential concern for students to pay for courses even register. My suggestion is to show Udacity's promotion policy ahead of user registration (such as 50% money back if finished within 1 year). If users can be aware of all the incentives ahead of payment, or even registration, then there might have less early cancellation.

So my null hypothesis is by showing a detailed promotion/offers (such as get half back when completing within one year) will not statistically increase net conversion .

The alternate hypothesis is by showing a promotions will increase the net conversion significantly.

This experiment will be posed to students in two groups: in the experiment group, the popup message of promotions will be shown to the experiment group, whereas the control group, no messages will be shown.

The unit of diversion is number of cookies, because number of cookies is prior to the experiment.

The invariant metric is number of cookies, because people will not see any messages before they browse the page.

The evaluation metric I chose is Retention because it can be measured what is the ratio of the number of users who enrolled, make their first payment. 

I hope to see statistically significant number of increase in the experiment group

