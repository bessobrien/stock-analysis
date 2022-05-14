# VBA Stock Analysis

## Overview of Project

We prepared a stock analysis code, and our client Steve, really liked it; it provided the results what he was looking for which was the ticker, Total Daily Volume, and the return rate - based on the year chosen in the input box.

However, now Steve wants to expand the abilities of the analysis to look through a possible thousands of stocks instead of just 12. For this project, we spent time to refactor the VBA code we came up with originally. We wanted to find a solution that might be a little faster as we increase the size of the data set.

## Results

We started with the original All Stocks Analysis code and ran the code for both the year 2017 and 2018. The timed results of the code-run for the original code for 2017 and 2018 was:

![Original_Time_2017](https://github.com/bessobrien/stock-analysis/blob/master/Resources/Original_Time_2017.png)

![Original_Time_2018](https://github.com/bessobrien/stock-analysis/blob/master/Resources/Original_Time_2018.png)

One note is that in the original code, we used nested For loops to run through each row of the data 12 times. Here is a snapshot of the original nexted loops:

![Original_Script_Nested](https://github.com/bessobrien/stock-analysis/blob/master/Resources/Original_Script_Nested.png)

### Refactoring the Code

We really wanted to see if we could refactor the code to run faster - in the anticipation that we might use this code for a much larger dataset in the future. While refactoring, we found that the nested loops were a big part of the time expended to run the code. So instead, we split up the loops: one loop to set all ticker indexes and volumes to 0, and then the main code which then only ran through the rows once (instead of 12 times!).

Here is a snapshot of the nested loops split out in the refactored code:

![Refactored_Script_Loops](https://github.com/bessobrien/stock-analysis/blob/master/Resources/Refactored_Script_Loops.png) 

We found that by splitting up the loops, we were able to decrease the code run time significantly. After our refectored script, our code run times for 2017 and 2018 were:

![VBA_Challenge_2017](https://github.com/bessobrien/stock-analysis/blob/master/Resources/VBA_Challenge_2017.png)

![VBA_Challenge_2018](https://github.com/bessobrien/stock-analysis/blob/master/Resources/VBA_Challenge_2018.png)

Our analysis results were the same for both the original code and the refactored code: 

![Analysis_Result_2017](https://github.com/bessobrien/stock-analysis/blob/master/Resources/Analysis_Result_2017.png) 

![Analysis_Result_2018](https://github.com/bessobrien/stock-analysis/blob/master/Resources/Analysis_Result_2018.png)

## Summary

We were able to successfully decrease our code run time with our refactoring. We believe that this script is now ready to run analysis on larger datasets.

**Advantages of refactoring are:**

1. Easier to maintain and read
2. Faster scripts
3. Less complex

**Disadvantages of refactoring are:**

1. Time consuming to refactor
2. Could be confusing if original script is large or does not run smoothly

In this particular project, we were able to decrease the time in which the script was able to run. In our refactoring project, we saw the results of advantage (faster scripts). We also saw a disadvantage realize in the project as well - it took quite a bit of time to figure out a solution that decreased the time. Overall, a success!
