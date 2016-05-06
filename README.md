#Summary

I have used the data from Prosper Loans to show which factors can relate to whether a loan will be paid completely, chargedoff, defaulted or past due. 

#Design
For my first graph, since I am showing relationship between two categorial variables (Loan Status and Credit Grading), a grouped bar chart seems to be a good choice. 

For the second graph, since I am showing relationship between a continuous and categorical variables(Debt-to-income ratio and Loan Status), a boxplot is good in order to compate the medians and the trends per catogory (Loan Status).

#Feedback
##Feedback1
####from Luke Wicent Sy
Regarding Credit Grading Feature,

Your graph makes sense, and I believe that it is indeed a good indicator whether a loan is likely to be completed, chargedoff, or defaulted.
If you can add how many percent with credit AA (and other credit grading too), a) defaulted, b) chargedoff, or c) completed, the story will be more numerically convincing.

Regarding DebtToIncomeRatio,

Your graph do tell that DebtToIncomeRatio has potential to be a good indicator, but not as strong as "Credit Grading".
Cancelled has a lower DebtToIncomeRatio than Completed. Is that relevant to the story? If not, why is it in the graph? Will there be issues if it is removed from the graph?
The median of Completed is indeed slightly lower than the other status. But you can still see that there are a lot of intersects with the range of DebtToIncomeRatio. Without knowing how each status is distributed (gaussian? normal? high concentration above? etc), its really hard to tell. 
Following your reasoning with the medians, DebtToIncomeRatio may be a good indicator to distinguish "Completed" from "Chargedoff" and "Defaulted", but not to distinguish "Chargedoff" from "Defaulted".

##Feedback2
####from David Smith
For your charts, I think the top one would better if you could show charged-off and delinquent (which, together, I call non-performing) as a percentage of the total number of loans. To me, showing the loan counts isn't as valuable as illustrating the riskiness of each credit grading. The higher the percentage of loans that go bad, the higher the risk.

Below the second one, you state "loan status has a strong relationship with debt-to-income ratio." The chart as it is drawn doesn't illustrate that very dramatically. Instead, there are a lot of overlapping confidence intervals. Seems to me like you could just as easily say the opposite. You also state, "Loans that were completed has a lower Debt-to-income ratio median compared to chargedoff, defaulted
and past due loans." That's true, but if you did an ANOVA test or pair-wise student t-tests with those other statuses, would "completed" be statistically different than those others? So I'm not sure how I would fix this one, except to say I would either change the narrative to more accurately describe the data, or find a different relationship that is more dramatic and interesting.﻿


#Resources

* D3.js Boxplot with Axes and Labels

http://bl.ocks.org/jensgrubert/7789216

* Vert Stacked Grouped Bar

http://dimplejs.org/examples_viewer.html?id=bars_vertical_grouped_stacked

* Udacity's Discussion Forum

https://discussions.udacity.com/t/creating-boxplot-using-d3-js/165568

https://discussions.udacity.com/t/error-cannot-read-property--hascategories-of-null/167169/5

https://discussions.udacity.com/t/x-axis-label-is-not-showing/167146/3
