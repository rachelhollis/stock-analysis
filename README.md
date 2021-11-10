# Stock Analysis

## Overview

Writing and executing code on the first attempt is not always the best way to accomplish a task. A key part of coding is refactoring code. The goal of refactoring code is to make the existing code more efficient by taking fewer steps, using less memory, and/or improving the logic. This process can also be used to make the code easier to read for future users. 

### Purpose

The code developed does its job. However, it might not be efficient or work as well for thousands of stocks. The purpose of this analysis is to refactor the code and determine whether the scrip runs faster.  

## Analysis and Challenges

### Stock Analysis Results

![resources/2017](resources/2017.PNG) ![resources/2018](resources/2018.PNG)

Overall, 2017 had a higher return than 2018. Only one stock, TERP, in 2017 had a negative return. At the end of 2017, investing in alternative energy appears to be a smart move. However, the results from 2018 are shocking. All but two stocks have a negative return. Some, including DQ, have a high negative rate. DQ went from having a positive return rate of 199.45% to a negative rate of -62.60% despite having a drastic increase in Total Daily Volume. ENPH and RUN have a return rate of around 82%. Despite their high rates, the market appears to be volatile and would be a risky investment. 

#### Challenges

The data ranges significantly between the two years. This indicates there is a strong influence over the market. However, the data set does not have the necessary data for further analysis into why and what the cause could be.

### Refactoring

#### Portion of Old Code

![resources/old](resources/old.PNG)
![resources/VBA_Challenge_2017_pre](resources/VBA_Challenge_2017_pre.PNG) ![resources/VBA_Challenge_2018_pre](resources/VBA_Challenge_2018_pre.PNG)

The initial code written looped over the data set row by row, over and over to display the results. The use of only one array (ticker) presented the need to output the Ticker, Total Volume, and Return before the next iteration. This process lead to a higher execution time of around 67000 seconds

#### Portions of New Code

![resources/output_array](resources/output_array.PNG)

Instead of one array, when refactoring the code three output arrays were added. This allowed the values for each ticker to be stored based on a the tickerIndex.

![resources/new](resources/new.PNG)

The refactored code allows it to loop once through the data and output the Ticker, Total Daily Volume, and Return to the corresponding arrays. After the loop through the data is finished, a loop through the arrays will output the required data by calling on the related tickerIndex for each value. 

This process is not only more efficient, but allows the values to be stored and called upon later. 


![resources/VBA_Challenge_2017](resources/VBA_Challenge_2017.PNG) ![resources/VBA_Challenge_2018](resources/VBA_Challenge_2018.PNG)

After refactoring, the execution time decreases dramatically. The average run time for the new code is around .20 seconds. In comparison to the previous running time of 67000, this is significantly more efficient. Where as the previous code worked well with a relatively small dataset, the new code will work better when analyzing a much bigger dataset i.e. the whole stock market.

#### Results


