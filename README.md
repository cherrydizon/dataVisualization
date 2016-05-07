#Summary

I have used the data from Prosper Loans to show which factors can relate to whether a loan is likely be paid successfully or not. My charts show that Credit Grading and Debt-to-income ratio are important factors when it comes to predicting the outcome of a loan.

#Design
####Initial Design
For my first graph, since I am showing relationship between two categorial variables (Loan Status and Credit Grading), a grouped bar chart seems to be a good choice. I showed the total number of loans per Loan Status grouped by the Credit Grading. I included a legend so that the reader can understand the trend of loan statuses per Credit Grading.

For the second graph, since I am showing relationship between a continuous and categorical variables(Debt-to-income ratio and Loan Status), a boxplot is good in order to compate the medians and the trends per catogory (Loan Status).

Since I will be comparing amounts across loan statuses, I used planer as visual encodings for my two graphs.

####Changes After Getting Feedback
1. For my first graph, in order to show a stronger trend, instead of the total number of loans as the y-axis, I used percentage per each Credit Grading.
2. For the second graph, I reduced the categories in my x-axis. This is to let my charts focus on loans that are already closed. Like what I initially did in my first graph, I just focused on completed, defaulted and chargedoff loans. 
3. I edited the description in the first graph. I added an explanation about the credit grading.
4. I edit the description in the second graph. My initial description wasn't really describing the data accurately. So I edited it and considered not just about the median but also the IQR.
5. I adjusted the positioning of the texts. The width of my initial design was too wide so I reduced it.
6. I added a link of Prosper Loans' website.
7. I adjusted the size of the texts. Some texts were in bold but small so I made them bigger.

#Feedback
##Feedback1
####from MS Computer Science student Luke Sy
Regarding Credit Grading Feature,

Your graph makes sense, and I believe that it is indeed a good indicator whether a loan is likely to be completed, chargedoff, or defaulted.
If you can add how many percent with credit AA (and other credit grading too), a) defaulted, b) chargedoff, or c) completed, the story will be more numerically convincing.

Regarding DebtToIncomeRatio,

Your graph do tell that DebtToIncomeRatio has potential to be a good indicator, but not as strong as "Credit Grading".
Cancelled has a lower DebtToIncomeRatio than Completed. Is that relevant to the story? If not, why is it in the graph? Will there be issues if it is removed from the graph?
The median of Completed is indeed slightly lower than the other status. But you can still see that there are a lot of intersects with the range of DebtToIncomeRatio. Without knowing how each status is distributed (gaussian? normal? high concentration above? etc), its really hard to tell. 
Following your reasoning with the medians, DebtToIncomeRatio may be a good indicator to distinguish "Completed" from "Chargedoff" and "Defaulted", but not to distinguish "Chargedoff" from "Defaulted".

##Feedback2
####from fellow Udacity student David Smith
For your charts, I think the top one would better if you could show charged-off and delinquent (which, together, I call non-performing) as a percentage of the total number of loans. To me, showing the loan counts isn't as valuable as illustrating the riskiness of each credit grading. The higher the percentage of loans that go bad, the higher the risk.

Below the second one, you state "loan status has a strong relationship with debt-to-income ratio." The chart as it is drawn doesn't illustrate that very dramatically. Instead, there are a lot of overlapping confidence intervals. Seems to me like you could just as easily say the opposite. You also state, "Loans that were completed has a lower Debt-to-income ratio median compared to chargedoff, defaulted
and past due loans." That's true, but if you did an ANOVA test or pair-wise student t-tests with those other statuses, would "completed" be statistically different than those others? So I'm not sure how I would fix this one, except to say I would either change the narrative to more accurately describe the data, or find a different relationship that is more dramatic and interesting.

##Feedback3
####from fellow Udacity student laurent_319928
You found an interesting topic!

I would suggest the following:

a/ Narrow the width of the html body otherwise the lines of the text are much too long.
To paraphrase The Not So Short Introduction to LATEX 2
The line length has to be short enough not to strain the eyes of the reader, while long enough to fill the page beautifully.

b/ "which factors you should carefully check before you get a loan"
shouldn't it be "before you request / ask for a loan" ? if you get a loan, it is already too late.

c/ you made the first sentence bold, to emphasize it, I suppose; the next one, starting with "As the credit..." is not bold any longer, but the font size seems to be somewhat larger; this is counter-intuitive.

d/ I would add some space between the first sentence and the first chart.

e/ "The credit grading system": I would welcome a hyperlink for those wondering whether it is free, accessible from the net, ...

f/ second chart: I would place the title above the chart and not in the chart.

g/ "when it comes to predicting the performance of a loan"
-> "when it comes to predicting the outcome of a loan" (might be a false alarm since I am not a native English speaker).

##Feedback4
####from fellow Udacity student karthik_403523
good work @Cherry 

What do you notice in the visualization?
regardless of Credit Grading number of loan completed is high. which is good for investors.

What questions do you have about the data?
if i was provided with details on what is AA ,A, B means it will be each for me to relate but as of now they are just some random alphabets to me.

What relationships do you notice?
It is little confusing the way the categories in x-axis are order. i guess it is order in alphabetic starting from 'c' - Cancelled to pastdue. this will be better if you order something starts with loan completion and goes till pastdue i think that way it will be easy to visualize and find trend since the variation in mean of each category is very less.

Is there something you don’t understand in the graphic?
the first graph was awesome and did it part. The title in the second graph is over lapping with the graph. if your are using dumple.js to create title, i would suggest you not to use them instead add a paragraph tags just before the graph tag and give the title name that it will stay out of the graph and use center tags to center the title.

good job !!

#Resources

* D3.js Boxplot with Axes and Labels

http://bl.ocks.org/jensgrubert/7789216

* Vert Stacked Grouped Bar

http://dimplejs.org/examples_viewer.html?id=bars_vertical_grouped_stacked

* Udacity's Discussion Forum

https://discussions.udacity.com/t/creating-boxplot-using-d3-js/165568

https://discussions.udacity.com/t/error-cannot-read-property--hascategories-of-null/167169/5

https://discussions.udacity.com/t/x-axis-label-is-not-showing/167146/3

*HTML Tutorial

http://www.w3schools.com/html/default.asp
