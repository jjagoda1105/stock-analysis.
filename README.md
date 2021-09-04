# stock-analysis.
## Refactoring the code 

### Overview of Project

The stock analysis provides us with a summary of all tickers and their performance for 2017 and 2018 based on their return value and the trading volume. At the beginning of this module we were presented with the raw data for every day each stock was traded. Our goal is to summarize all the tickers’ performance in the most efficient way possible, by using VBA code. We will use what we learned in module 2, to create a faster code that will summarize our tickers’ performance. 

### Analysis of ticker performance

All of the tickers performed much better in 2017. DQ performed the best in 2017 based on its return of 199.4%, however in 2018 DQ performed the worst with a return of -62.5%. It is important to consider both years and all stocks when looking at the stock performance that way we can base our conclusion on all relevant factors. With that being said, we would not want to invest in DQ, because in the following year during 2018, it did not do well. We want to pick a stock that is less volatile. Let’s take a look at 2018 stocks shown below:

As you can see, in 2018, several stocks had a negative return, so DQ was not alone. This is why it is important to compare all the stocks to each other. We can see that several other stocks had bad performance, so it potentially could have just been a bad year for all stocks in general. ENPH had the best performance over the past two years based on the return percentage, because it was the had the highest average return for both 2017 and 2018.

### Analysis of code Used 

Our code was able to compare all the stocks’ volumes and starting prices based on their different ticker values. The original code looped through the tickers first, and then looped through all the rows within that ticker. The advantage of this, is that it is more straight forward to think this way. The disadvantage of this code is that the nested loop makes the code take longer and it requires the computer to do more steps, see the nested loop below for reference. You can also see the time to run through the code was longer.  

On the other hand, the refactored code loops through all the rows and assigns a ticker index to go through each value in the ticker array. It does not use a nested loop, instead it uses the tickerindex to run through the rows based on the ticker element, see how I introduced the ticker index in the image below. The advantage of is that the code is condensed and faster, see the run time displayed in the image below and compare it to the run time above. The disadvantage of this, is that introducing the tickerindex can introduce more bugs, which it did, and I had to solve new problems.

### Analysis of Code Refactoring

The main advantage of refactoring the code is that we were able to make it run faster and do the work more effectively. The code took .7 seconds longer before it was refactored. Additionally, we made the code simpler which can benefit a person who might want to edit this code again. 

On the other hand, refactoring can be time consuming to create and hard to think through the logic and there is a possibility to introduce more bugs into the code, like what happened when I was doing this. All in all, it was worth it because now the code is much better quality. 
