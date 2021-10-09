# Analyze-A-B-Test-Results
###### **Udacity Data Analyst Degree - Project**
## Overview
A/B tests are very commonly performed by data analysts and data scientists.
For this project, I will be working to understand the results of an A/B test run by an e-commerce website. The company has developed a new web page to increase the number of users who "convert," meaning the number of users who decide to pay for the company's product. My goal is to work through the Jupyter Notebook to help the company understand if they should implement this new page, keep the old page, or perhaps run the experiment longer to make their decision.

## What Software Do I Need?

**For this project, the following software requirements apply:**
- You should have: 
  - Python 3, NumPy, random, statsmodels.api, matplotlib.pyplot, and pandas installed using Anaconda.
  - A text editor, like Atom.
  - A terminal application (Terminal on Mac and Linux or Cygwin on Windows).
- Or Jupyter Notebook.

## The Datasets
**The ab_data.csv data file core columns:**
- user_id 
- timestamp 
- group
- landing_page
- converted 

**The countries.csv data file have the following two columns:**
- user_id
- country

## The Files
**For guiding you through this project, comments are provided in the Analyze_ab_test_results_notebook.ipynb file. You will need these files:**
- ab_data.csv
- countries.csv

## Project Parts:
- Part I - Probability
- Part II - A/B Test
- Part III - A regression approach

## Questions Answered
- What is the probability of an individual converting regardless of the page they receive?
- Given that an individual was in the control group, what is the probability they converted?
- Given that an individual was in the treatment group, what is the probability they converted?
- What is the probability that an individual received the new page?
- Explain whether the new treatment group users lead to more conversions.
- If you want to assume that the old page is better unless the new page proves to be definitely better at a Type I error rate of 5%, what should be your null and alternative hypotheses ( 𝐻0  and  𝐻1 )?
- What is the conversion rate for  𝑝𝑛𝑒𝑤  under the null hypothesis?
- What is the conversion rate for  𝑝𝑜𝑙𝑑  under the null hypothesis?
- What is  𝑛𝑛𝑒𝑤 , the number of individuals in the treatment group?
- What is  𝑛𝑜𝑙𝑑 , the number of individuals in the control group?
- Find the difference in the "converted" probability  (𝑝′𝑛𝑒𝑤  -  𝑝′𝑜𝑙𝑑)  for your simulated samples.
- Re-create new_page_converted and old_page_converted and find the  (𝑝′𝑛𝑒𝑤  -  𝑝′𝑜𝑙𝑑)  value 10,000 times using the same simulation process.
- Plot a histogram of the p_diffs. Does this plot look like what you expected?
- What proportion of the p_diffs are greater than the actual difference observed in the df2 data?
- What does the p-value signify in terms of whether or not there is a difference between the new and old pages?
- Use sm.stats.proportions_ztest() to compute your test statistic and p-value.
- What do the z-score and p-value you computed in the previous question mean for the conversion rates of the old and new pages?
- What type of regression should you be performing in this case? 
- Use statsmodels to instantiate your regression model on the two columns you created. above, then fit the model to predict whether or not an individual converts.
- Provide the summary of your model.
- What is the p-value associated with ab_page? Why does it differ from the value you found in Part II?
- Discuss why it is a good idea to consider other factors to add into your regression model. 
- Are there any disadvantages to adding additional terms into your regression model?
- Now along with testing if the conversion rate changes for different pages, also add an effect based on which country a user lives in.
- Though you have now looked at the individual factors of country and page on conversion, we would now like to look at an interaction between page and country to see if are there significant effects on conversion. Create the necessary additional columns, and fit the new model.
- Provide the summary results (statistical output), and your conclusions (written response) based on the results.


## Conclusion:
- Part I: 
  - The "converted" probability for the old page is slightly higher than that of the new page so the new treatment group users didn't lead to more conversions.
- Part II: 
  - As the z_score is less than z_o.05 we failed to reject the null hypothesis.
  - With the resulted p_value we failed to reject the null hypothesis with regard to the type I error threshold.
  - The computed z-score and p-value agree with the findings in parts j. and k.
- Part III: 
  - With the resulted p_value for the 'ab_page' we failed to reject the null hypothesis with regard to the type I error threshold.
  - As none of the p-values is below the error rate of 0.05, the country had no impact on conversion.
  - Based on the statistical results from the available data analysis, I think it is better to continue with the old page as there is no evidence or indication for better results with the new page.
