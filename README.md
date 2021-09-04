# stock-analysis.
## Refactoring the code 

### Overview of Project

The stock analysis provides us with a summary of all tickers and their performance for 2017 and 2018 based on their return value and the trading volume. At the beginning of this module we were presented with the raw data for every day each stock was traded. Our goal is to summarize all the tickers’ performance in the most efficient way possible, by using VBA code. We will use what we learned in module 2, to create a faster code that will summarize our tickers’ performance. 

### Analysis of ticker performance
#### 2017 Stocks
![All Stocks 2017](https://user-images.githubusercontent.com/88689043/132105947-499814c9-877c-40a5-9e07-0d5eea82d37e.PNG)

All of the tickers performed much better in 2017. DQ performed the best in 2017 based on its return of 199.4%, however in 2018 DQ performed the worst with a return of -62.5%. It is important to consider both years and all stocks when looking at the stock performance that way we can base our conclusion on all relevant factors. With that being said, we would not want to invest in DQ, because in the following year during 2018, it did not do well. We want to pick a stock that is less volatile. Let’s take a look at 2018 stocks shown below:

#### 2018 Stocks
![All Stocks 2018](https://user-images.githubusercontent.com/88689043/132105940-991aa515-60fe-4165-9406-35cf93835c64.PNG)

As you can see, in 2018, several stocks had a negative return, so DQ was not alone. This is why it is important to compare all the stocks to each other. We can see that several other stocks had bad performance, so it potentially could have just been a bad year for all stocks in general. ENPH had the best performance over the past two years based on the return percentage, because it was the had the highest average return for both 2017 and 2018.

### Analysis of code Used 

#### Original Code
Our code was able to compare all the stocks’ volumes and starting prices based on their different ticker values. The original code looped through the tickers first, and then looped through all the rows within that ticker. The advantage of this, is that it is more straight forward to think this way. The disadvantage of this code is that the nested loop makes the code take longer and it requires the computer to do more steps, see the nested loop below for reference. You can also see the time to run through the code was longer.  

![nested loop original](https://user-images.githubusercontent.com/88689043/132105965-55c42203-3b8f-43af-bcdd-60d04ca096c4.PNG)
![2018 runtime slow](https://user-images.githubusercontent.com/88689043/132105977-27537592-e51c-46ac-be27-c2bc6a0a1763.PNG)

##### Refactored Code
On the other hand, the refactored code loops through all the rows and assigns a ticker index to go through each value in the ticker array. It does not use a nested loop, instead it uses the tickerindex to run through the rows based on the ticker element, see how I introduced the ticker index in the image below. The advantage of is that the code is condensed and faster, see the run time displayed in the image below and compare it to the run time above. The disadvantage of this, is that introducing the tickerindex can introduce more bugs, which it did, and I had to solve new problems.

![code picture refactored](https://user-images.githubusercontent.com/88689043/132105992-76e006fc-17a0-421d-aa17-0de591d58f62.PNG)
![2018 runtime](https://user-images.githubusercontent.com/88689043/132106000-486cdede-c381-4581-aacf-f9bc1a1653cd.PNG)

### Analysis of Code Refactoring
#### Advantage
The main advantage of refactoring the code is that we were able to make it run faster and do the work more effectively. The code took .7 seconds longer before it was refactored. Additionally, we made the code simpler which can benefit a person who might want to edit this code again. 
#### Disadvantage
On the other hand, refactoring can be time consuming to create and hard to think through the logic and there is a possibility to introduce more bugs into the code, like what happened when I was doing this. All in all, it was worth it because now the code is much better quality. 
