# Module 15 - MechaCar Challenge
# Statistics & R
 
## DELIVERABLE 1: Linear Regression to Predict MPG

- Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
The vehicle-length and vehicle ground clearance are statistically likely to provide non-random amounts of variance to the model and these two variables/coefficients have a significant impact on miles per gallon on the MechaCar prototype. Conversely, the vehicle weight, spoiler angle and AWD have p-values that indicate a random amount of variance with the dataset.

- Is the slope of the linear model considered to be zero? Why or why not?
The p-value for this model: p-value: 5.35e-11, is much smaller than the assumed significance level of 0.05%.  This indicates that there is sufficient evidence to reject our null hypothesis and that the slope of this linear model is not zero.

- Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
This linear model has a R-squared value of 0.7149, which means that approximately 71% of all mpg predictions will be determined by this model. Or, the multiple regression model does predict mpg of MechCar prototypes effectively.

Insert fig 1

If we remove the less impactful independent variables/coefficients like vehicle weight, spoiler and and AWD, then the precidtcability does decrease, but not drastically.  The R-squared value falls from 0.7149 to 0.674. 

Insert fig 2

## DELIVERABLE 2: Summary Statistics on Suspension Coils

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

The Supension_Coil dataset contains results of testing various weight capacitites of multiple suspension coils from multiple production lots to determine consistency.

### Total Summary for all manufacturing lots"
Insert fig 3

### Lot Summary for these specific lots:
Insert fig 4

The variance of the coils is 62.29 PSI for the entire population (total summary) of 150 coils, which is well within the specification of 100 PSI.

Looking at the lot summary, the variance of lots 1 and 2 are 0.98 and 7.47 respectively, which are well within the specification of 100 PSI, whereas lot 3 has a variance of 170.29 which is way pover than the desired specification. 

## DELIVERABLE 3: T-Tests on Suspension Coils
Using your knowledge of R, perform t-tests to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.

The t-test on the suspension coil dataset to determine whether therre is a statistical difference between the mean of the provided dataset and the hypothesized population datas with a population mean of 1500 shows the following summary for ALL manufacturing lots:

Insert fig 5

The true mean of the sample is 1497.51, with a p-value of 0.06, which is higher than the siginificance level of 0.05.  This means that there is not enough evidence to support rejecting the null hypothesis.  The mean of all three of the manufacturing lots is statistically similar to the presumes popluation mean of 1500.05.

Now, looking at each of the individual lots:

Insert fig 6

- Lot 1 has a true sample mean of 1500 with a p-value of 1 which indicates that we cannot reject the null hypothesis and that there is no statistical difference between the observed sample mean and the popluation mean of 1500.

- Lot 2 has a sample mean 1500 with a p-value of 0.61 which indicates that the null hypothesis cannot be rjected and that the sample mean and the popluation mean of 1500 are statistically similar.

- However, Lot 3 is different from lots 1 and 2.  Lot 3 has a sample mean of 1496.14 with a p-value of 0.04, which is lower than significance level of 0.05.  This indicates to reject the null hypothesis and indicating that the sample mean and the popluation mean are not statistically different. 

It is possible that something went worng/different in lot 3 production cycle.  This process needs to be checked for any system failure and the suspension coils from lot 3 need to be inspected and removed if not meeting the desired quality requirements. 

## DELIVERABLE 4: Study Design comparing the MechaCar to the Competition

A statistical study can be conducted to determine if we can predict values for the maintenance cost using a linear model and values from cost.

Analyzing the relationship of cost and maintenace cost would help choose the best ratio. This would quantify how the vehicle performs against the competition by providing potential profit margins for the company.

Then, we can test the R-squared value to determine the likelihood that future data points will fit the linear model. The null hypothesis is that the slope of the linear model is zero and the alternative hypothesis is that the slope of the linear model is NOT zero.

Then, a simple linear regression can be used to test the hypothesis because it will provide a meaningful model to be used in finding the optimal cost for the MechaCar while minimizing maintenance cost to increase consumer interest.

The data needed to perform this study would be the cost and maintenacne cost of MechaCar prototypes.

