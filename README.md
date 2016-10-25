# Final Project: Design an A/B test

## Experiment Design

### Metric Choice
The invariant metrics I used are: Number of cookies, Number of clicks.

The evaluation metrics I used are: Gross conversion, Retention, and Net conversion.

For each metric:

Number of cookies: I chose it as invariant metric because when users browse the webpage, he/she already has one unique browser id. Thus it is independent.

Number of user-ids: user-ids are people who registered the course. Thus it depends on the people who enrolled the free trial. So I didn't choose it as invariant metric.
I didn't choose it to be evaluation metric because the user-ids may be screwed from the experiment group.

Number of clicks: I chose it as invariant metric because people need to click, then he/she can see the content/experiment.

Click-through-probability: It could be a good invariant metric but I prefer the pure numbers instead of probability for invariant metric.

Gross conversion: I choose it as evaluation metric because user-ids are dependent on the effect of the experiment and divided by the number of unique cookies can prevent from unbiased/unbalanced data.

Retention: I didn't use it since the experiment might affect users who is in free trial.

Net conversion: same reason as above -- the number of people enrolled in the free trail devided by the number of unique cookies can prevent from unbalanced data.


### Measuring Standard Deviation
Goss conversion: 0.0202

Net conversion: 0.0156

Gross conversion, retention, and net conversion are percentages, I treat it as unit of diversion. 

### Sizing
#### Number of sample vs. power

I did not use the Bonferroni correction. And I used Gross conversion, Retention, and Net conversion as evaluation metrics.
I would need 685325 pageviews for a test of alpha = 0.05 and beta = 0.2.

#### Duration vs. Exposure

Since this experiment won't jeopardise Udacity's current business, I would divert 100% to this experiment. And would roughly need 18 days to complete the experiment.

Since I don't see any downside or side effects of this diversion.

## Experiment Analysis
### Sanity Checks

No Bonferroni correction

Number of cookies: Lower bound - 0.4988, Upper bound - 0.5011, Observed - 0.5006. It passes the Sanity Checks.

Number of clicks: Lower bound - 0.4959, Upper bound - 0.5041, Observed - 0.5005. It passes.

### Result Analysis
#### Effect Size Tests

No Bonferroni correction

Gross conversion: Lower bound - -0.0291, Upper bound - -0.0120. Since 0 is not included, it is statistical significance and practical significance.

Net conversion: Lower bound - -0.0116, Upper bound - 0.0019, since 0 is included, it is not significant.

#### Sign Tests

No Bonferroni correctionu

Gross conversion: p-value - 0.0026. It is statistical significant 

Net conversion: p-value - 0.6776. It is not significant.

#### Summary

I didn't use Bonferroni correction since there aren't too many variables to test. If we want to further segment it, we can incorporate Bonferroni correction.

### Recommendation

Since Net conversion has 0 in the confidence interval, it is not significant. And it contains negative values, it might cause some warry regarding carry this experiment. However, we can redesign some other designs before experiment.

## Follow-Up Experiment

Udacity was not extremely clear when first time users sees it, since it is not like most mooc platform: by offer a codesigned nanodegree. But it charges by month, which would intimate some users, probably not even want to initiate the registration.

So my null hypothesis is by showing a detailed promotion/offers (such as get half back when completing within one year) will not statistically increase Retention.

The unit of diversion is user-id, because we want to track if promotions will attrack more users to register.

The invariant metric is number of people registered.

The evaluation metric I chose is Retention.

If the result comes back positive, and significant both practically and statistically, we are safe to launch the new feature.


