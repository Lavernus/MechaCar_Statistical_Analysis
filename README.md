# Statistical Analysis of MechaCars
## Linear Regression to Predict MPG
![Linear_Reg.png](https://github.com/Lavernus/MechaCar_Statistical_Analysis/blob/main/Images/Linear_Reg.png)

Of the variables used to calculate the linear regression, we can see that the vehicle length, ground clearance, and intercept are the only variables to introduce a non-random amount of variance to the mpg of the cars. Since the p-value of the linear regression is 5.35e-11, which is much smaller than our assumed significance level of 0.05%, there is enough evidence to say the slope of the linear model is not zero. Looking at the Multiple R-squared we can see that around 71.5% of the variability of the cars' mpg can be explained using this linear model. Using Pearson's Correlation, we can see that the linear model can predict the mpg of the prototype cars effectively since the independent variables have a strong correlation with the dependent variable, with the absolute r value being above 0.7. 
## Summary Statistics on Suspension Coils
![total_summary.png](https://github.com/Lavernus/MechaCar_Statistical_Analysis/blob/main/Images/total_summary.png)

For all manufacturing lots we can see that the variance of the suspension coils does not exceed the 100 pounds per square inch threshold, since the summary table displays 62.3 pounds per square inch variance. 

![lot_summary.png](https://github.com/Lavernus/MechaCar_Statistical_Analysis/blob/main/Images/lot_summary.png)

When we look at the individual lot summaries, however, we can see that while the first two lots are well below the variance threshold at 0.98 and 7.47 pounds per square inch respectively, lot 3 is way over the threshold at 170.3 pounds per square inch.
## T-Tests on Suspension Coils
![Total_T.png](https://github.com/Lavernus/MechaCar_Statistical_Analysis/blob/main/Images/Total_T.png)

The first t-test we will look at is the test for the PSIs across all manufacturing lots. The p-value is slightly above our assumed significance level of 0.05 at 0.06, which means that we do not have sufficient evidence to reject the null hypothesis. This means that the two means are statistically similar.

![1_T.png](https://github.com/Lavernus/MechaCar_Statistical_Analysis/blob/main/Images/1_T.png)

For Lot 1 specifically, we see that the p-value is 1. Again, since it is above 0.05, we do not have sufficient evidence to reject the null hypothesis and the two means are statistically similar. 

![2_T.png](https://github.com/Lavernus/MechaCar_Statistical_Analysis/blob/main/Images/2_T.png)

Lot 2 has similar results as Lot 1, with the p-value being 0.6 which is above 0.05. This means we do not have sufficient evidence to reject the null hypothesis and the two means are statistically similar.

![3_T.png](https://github.com/Lavernus/MechaCar_Statistical_Analysis/blob/main/Images/3_T.png)

Lot 3 is the only t-test that has a p-value below 0.05 at 0.04. This means that we do have sufficient evidence to reject the null hypothesis and the two means are statistically different.

## Study Design: MechaCar vs Competition
In order to compare the MechaCar versus its competition, we need to test multiple metrics that the consumer would be interested in. Comparing the amount of money required to afford either would be a good place to start, so the metrics of the MechaCar and the competition measured will be the upfront cost of the vehicle, the maintenance cost, and the fuel efficiency for both highway and city.

Since we're comparing the two groups: MechaCars and its competition's cars, we will need a null hypothesis and alternative hypothesis pertaining to the statistical significance of the difference in the means of these two groups. This means that our null hypthesis is that the difference in group means is zero, and the alternative hypothesis is that the difference in group means is different from zero. 

Now that we have the hypotheses, we can test them. By doing multiple, two-sample t-tests we would be able to determine the statistical difference between the distribution means of each metric for MechaCars and its competition's cars. For example; we could conduct a two-sample t-test on the MechaCars' mean cost and the competitions' mean cost. If the p-value is less than our assumed significance level, we can assume that the two means are statistically different, meaning that our alternative hypothesis is correct. If the p-value is higher, the two means are statistically similar, meaning our null hypothesis is correct. We could then conduct two-sample t-tests on the other metrics in the same manner. Doing these two-sample t-tests would allow us to determine whether the difference in the MechaCars and its competition's cars is large enough to effectively decide whether either group costs more money to own. 

The data in these t-tests are as follows: the independent variables are the two groups being tested; MechaCars and the competitions' cars. These independent variables are dichotomous, since it can be either MechaCars or the competitions' cars. The dependent variables are the means of each group's metric which is being tested at the moment, which are continuous since it is a number that could be any value.
