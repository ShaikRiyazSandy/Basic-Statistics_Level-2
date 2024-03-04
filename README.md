# Assignment Advance Stats sets(1-4)


# Assignment set-1

# Topics: Descriptive Statistics and Probability


	Look at the data given below. Plot the data, find the outliers and find out  μ,σ,σ^2

Name of company	Measure X\
Allied Signal	24.23%\
Bankers Trust	25.53%\
General Mills	25.41%\
ITT Industries	24.14%\
J.P.Morgan & Co.	29.62%\
Lehman Brothers	28.25%\
Marriott	25.81%\
MCI	24.39%\
Merrill Lynch	40.26%\
Microsoft	32.95%\
Morgan Stanley	91.36%\
Sun Microsystems	25.99%\
Travelers	39.42%\
US Airways	26.71%\
Warner-Lambert	35.00%\
	
  
The following is the outlier in the boxplot: Morgan Stanley 91.36%
measure_x.describe()
Mean = 33.271333
Standard deviation = 16.945401
measure_x.var()
Variance = 287.1466123809524





	
 
Answer the following three questions based on the box-plot above.

	What is inter-quartile range of this dataset? (please approximate the numbers) In one line, explain what this value implies.
Ans: Approximately (First Quantile Range) Q1 = 5 (Third Quantile Range) Q3 = 12, Median (Second Quartile Range) = 7
(Inter-Quartile Range) IQR = Q3 – Q1 = 12 – 5 = 7 
Second Quartile Range is the Median Value

	What can we say about the skewness of this dataset?
Ans:  Right-Skewed median is towards the left side it is not normal distribution

	If it was found that the data point with the value 25 is actually 2.5, how would the new box-plot be affected?
Ans: In that case there would be no Outliers on the given dataset because of the outlier the data had positive skewness it will reduce and the data will normal distributed
	
 

Answer the following three questions based on the histogram above.
	Where would the mode of this dataset lie?
Ans: The mode of this data set lie in between 5 to 10 and approximately between 4 to 8 .

	Comment on the skewness of the dataset.	
Ans: Right-Skewed. Mean>Median>Mode

	Suppose that the above histogram and the box-plot in question 2 are plotted for the same dataset. Explain how these graphs complement each other in providing information about any dataset. 
Ans: They both are right-skewed and both have outliers the median can be easily visualized in box plot where as in histogram mode is more visible.


	AT&T was running commercials in 1990 aimed at luring back customers who had switched to one of the other long-distance phone service providers. One such commercial shows a businessman trying to reach Phoenix and mistakenly getting Fiji, where a half-naked native on a beach responds incomprehensibly in Polynesian. When asked about this advertisement, AT&T admitted that the portrayed incident did not actually take place but added that this was an enactment of something that “could happen.” Suppose that one in 200 long-distance telephone calls is misdirected. What is the probability that at least one in five attempted telephone calls reaches the wrong number? (Assume independence of attempts.)

Ans:  IF 1 in 200 long-distance telephone calls are getting misdirected.  
probability of call misdirecting   = 1/200
Probability of call not Misdirecting = 1-1/200 = 199/200
The probability for at least one in five attempted telephone calls reaches the wrong number
Number of Calls = 5
n = 5
p = 1/200
q = 199/200
P(x) = at least one in five attempted telephone calls reaches the wrong number
P(x) = ⁿCₓ pˣ qⁿ⁻ˣ
P(x) = (nCx) (p^x) (q^n-x)     # nCr = n! / r! * (n - r)!
P(1) = (5C1) (1/200)^1 (199/200)^5-1
P(1) = 0.0245037

	Returns on a certain business venture, to the nearest $1,000, are known to follow the following probability distribution
x	P(x)
-2,000	0.1
-1,000	0.1
0	0.2
1000	0.2
2000	0.3
3000	0.1
E(X) =Sum X.*P(X) | E(X^2) =X^2*P(X)
           -200                |          400000
          -100                 |          100000
             0                 |             0
           200                 |          200000  
           600                 |          1200000
           300                 |          900000
Total:     800                 |          2800000
	What is the most likely monetary outcome of the business venture?
Ans: The most likely monetary outcome of the business venture is 2000$
As for 2000$ the probability is 0.3 which is maximum as compared to others

	Is the venture likely to be successful? Explain
Ans:  Yes, the probability that the venture will make more than 0 or a profit
p(x>0)+p(x>1000)+p(x>2000)+p(x=3000) = 0.2+0.2+0.3+0.1 = 0.8 this states that there is a good 80% chances for this venture to be making a profit 

	What is the long-term average earning of business ventures of this kind? Explain
Ans:  The long-term average is Expected value = Sum (X * P(X)) = 800$ which means on an average the returns will be + 800$

	What is the good measure of the risk involved in a venture of this kind? Compute this measure
Ans: The good measure of the risk involved in a venture of this kind depends on the Variability in the distribution. Higher Variance means more chances of risk 
Var (X) = E(X^2) –(E(X))^2
             = 2800000 – 800^2
             = 2160000



# Assignment set-2

# Topics: Normal distribution, Functions of Random Variables

1.	The time required for servicing transmissions is normally distributed with  = 45 minutes and  = 8 minutes. The service manager plans to have work begin on the transmission of a customer’s car 10 minutes after the car is dropped off and the customer is told that the car will be ready within 1 hour from drop-off. What is the probability that the service manager cannot meet his commitment? 

A.	0.3875   
B.	0.2676   
C.	0.5   
D.	0.6987 \
Ans: ‘B’ 
 """the serving work will begin after 10 min of drop off so 45+10 
which will now take more than the usual time so new mew is 55 minutes 
and the probability that it will take more than 1 hour to complete""""
mew = 55
std = 8
q1 = 1-stats.norm.cdf(60, loc = mew, scale = std)
q1 = 0.2659
The probability that the service manager cannot meet his commitment is 0.2659


2.	The current age (in years) of 400 clerical employees at an insurance claims processing center is normally distributed with mean  = 38 and Standard deviation  =6. For each statement below, please specify True/False. If false, briefly explain why.
A.	More employees at the processing center are older than 44 than between 38 and 44.\
Ans: False.
Because the probability for employees at the processing center are more between 38 and 44 than older than 44.
mean = 38
std1 = 6
q2_lessthan_38 = stats.norm.cdf(38, loc = mean, scale = std1)
q2_lessthan_38 = 0.5
q2_less_than_44 = stats.norm.cdf(44, loc = mean,  scale = std1)
q2_less_than_44 = 0.841
q2_betweeen_38_and_44 = q2_less_than_44 - q2_lessthan_38
print('The probability of employee age between 38 and 44 is',np.round(q2_betweeen_38_and_44*100,2),'%')
The probability of employee age between 38 and 44 is 34.13 %
q2_morethan_44 = 1-stats.norm.cdf(44, loc = mean, scale = std1)
print('The probability of employee age more than 44 is',np.round(q2_morethan_44*100,2),'%')
The probability of employee age more than 44 is 15.87 %
true_or_false = (q2_morethan_44 > q2_betweeen_38_and_44)
print('Answer:',true_or_false)\
Answer: False

B.	A training program for employees under the age of 30 at the center would be expected to attract about 36 employees.\
Ans: True.
q2b = stats.norm.cdf(30, loc = mean, scale = std1)*100
print('A training program for employees under the age of 30 at the center would be expected to attract about',np.round((q2b*400)/100,0),'employees')
A training program for employees under the age of 30 at the center would be expected to attract about 36.0 employees

3.	If X1 ~ N(μ, σ2) and X2 ~ N(μ, σ2) are iid normal random variables, then what is the difference between 2 X1 and X1 + X2? Discuss both their distributions and parameters.\       
Ans:  
The Normal Distribution has its link with the Central Limit Theorem, which states that ‘Any large sum of independent identically distribution random variables are approximately Normal then
(X1 + X2) and (2X1) tends to have Normal distribution only If X1 and X2 are i.i.d and n is Large. 

The Difference between 2X1 and (X1 + X2) is the magnitude they hold of two different sample subsets (X1 and X2) from the same source(population). 
X1 and X2 can be a different subset of a sample from a similar source (population) but 
If X1 ~ N(μ, σ2)  then, 2 X1 ~ N(2 μ, 4 σ2 ) 
If X1 ~ N(μ, σ2) and X2 ~ N(μ, σ2) are iid normal random variables then 
(X1 + X2)~N(μ+ μ,  σ2+  σ2)~(2 μ, 2 σ2)
Hence, 2X1 – (X1+X2) ~(2 μ – 2 μ, 4 σ2  + 2σ2 )
The distribution remains the same for every sample subset of similar source, it tends to fall under Normal distribution and slight deviations in parameters.

The Normal distribution has two parameters, the mean, µ, and the variance, σ2.
 µ and σ2satisfy −∞ < µ < ∞, σ2> 0. We write X ∼ Normal (µ, σ2) or X ∼ N(µ, σ2 ).

4.	Let X ~ N(100, 202). Find two values, a and b, symmetric about the mean, such that the probability of the random variable taking a value between them is 0.99. \

A.	90.5, 105.9 \
B.	80.2, 119.8 \
C.	22, 78 \
D.	48.5, 151.5\ 
E.	90.1, 109.9\
Ans:  D. 
print("""The two values of a and b, symmetric about the mean, 
      are such that the probability of the random variable 
      taking a value between them is 0.99:""",np.round(stats.norm.interval(0.99, loc = 100, scale = 20),1))
The two values of a and b, symmetric about the mean, 
      are such that the probability of the random variable 
      taking a value between them is 0.99: [ 48.5 151.5]


5.	Consider a company that has two different divisions. The annual profits from the two divisions are independent and have distributions Profit1 ~ N(5, 32) and Profit2 ~ N(7, 42) respectively. Both the profits are in $ Million. Answer the following questions about the total profit of the company in Rupees. Assume that $1 = Rs. 45\

A.	Specify a Rupee range (centered on the mean) such that it contains 95% probability for the annual profit of the company.\
Ans: Rupee ranges in between [9.9 to 98.1] Crore Rupees, 95% of the time for the Annual Profit of the Company.

B.	Specify the 5th percentile of profit (in Rupees) for the company\
Ans: The 5TH Percentile of profit for the company is 17 Crore Rupees

C.	Which of the two divisions has a larger probability of making a loss in a given year?\
Ans: The Division #2 (Profit2 ~ N(7, 42) ) has a larger probability of making a loss in a given year



# Assignment set-3

# Topics: Confidence Intervals

1.	For each of the following statements, indicate whether it is True/False. If false, explain why.

I.	The sample size of the survey should at least be a fixed percentage of the population size in order to produce representative results.
Ans) True. The representation of the survey results should have a sample size. The sample size must be a fixed percentage of the total population size of the survey.

II.	The sampling frame is a list of every item that appears in a survey sample, including those that did not respond to questions.
Ans) False: The sampling frame refers to a list of items which respond to the question and not the ones which do not respond to the questions.

III.	Larger surveys convey a more accurate impression of the population than smaller surveys.
Ans) True: The larger convey a more accurate impression of the population as larger surveys involve large sample size which reduces the chances of error.

	
2.	PC Magazine asked all of its readers to participate in a survey of their satisfaction with different brands of electronics. In the 2004 survey, which was included in an issue of the magazine that year, more than 9000 readers rated the products on a scale from 1 to 10. The magazine reported that the average rating assigned by 225 readers to a Kodak compact digital camera was 7.5. For this product, identify the following:

A.	The population
Ans) Readers of the magazine=9000

B.	The parameter of interest
Ans) Rating of the camera(7.5)

C.	The sampling frame
Ans) Sampling frame, All readers of the issue where the survey was included

D.	The sample size
Ans) 225

E.	The sampling design
Ans) Voluntary response

F.	Any potential sources of bias or other problems with the survey or sample
Ans) It is possible that only those who were particularly pleased or only who are displeased with the product participated in the survey, which can make the results unreliable.
3.	For each of the following statements, indicate whether it is True/False. If false, explain why.

I.	If the 95% confidence interval for the average purchase of customers at a department store is $50 to $110, then $100 is a plausible value for the population mean at this level of confidence.
Ans) True. Confidence interval identifies the collection of values for the population parameter that are consistent with the observed sample.

II.	If the 95% confidence interval for the number of moviegoers who purchase concessions is 30% to 45%, this means that fewer than half of all moviegoers purchase concessions.
Ans) False. We have evidence in that direction, but we cannot confirm 100% based on this data. We must consider the values out of this range (i.e. more than 95% confidence interval).

III.	The 95% Confidence-Interval for μ only applies if the sample data are nearly normally distributed.
Ans) False. We should have a moderately large sample (usually at least larger than 30 for many cases), the central limit theorem implies that the sampling distribution is normal regardless of the data itself.


4.	What are the chances that  ?

A.	¼ 
B.	½ 
C.	¾ 
D.	1
Ans) ‘B’. This is a pure assumption. There is a 50% chance that the sample mean(X) is greater than the population mean (μ).


5.	In January 2005, a company that monitors Internet traffic (WebSideStory) reported that its sampling revealed that the Mozilla Firefox browser launched in 2004 had grabbed a 4.6% share of the market.

I.	If the sample were based on 2,000 users, could Microsoft conclude that Mozilla has a less than 5% share of the market?
Ans) X=0.046, n=2000, Z95=1.96, q=0.954
95% confidence interval for the proportion of web users using Mozilla is
=X+_Z*sqrt((X*q)/n)
=0.046+_1.96*sqrt((0.046*0.954)/2000)
=0.046+_0.00918
=0.0368-0.0551.

II.	WebSideStory claims that its sample includes all the daily Internet users. If that’s the case, then can Microsoft conclude that Mozilla has a less than 5% share of the market?
Ans) In this case, we have data on the entire population and the sample value accurately reflects the population number. Thus, we can conclude that the share is less than 5%.


6.	A book publisher monitors the size of shipments of its textbooks to university bookstores. For a sample of texts used at various schools, the 95% confidence interval for the size of the shipment was 250 ± 45 books. Which, if any, of the following interpretations of this interval are correct?

A.	All shipments are between 205 and 295 books.
Ans) Incorrect. The interval of (205,295) is for 95% confidence not for 100%.

B.	95% of shipments are between 205 and 295 books.
Ans) Incorrect. The interval doesn’t describe individual shipments.

C.	The procedure that produced this interval generates ranges that hold the population mean for 95% of samples.
Ans) Correct. 95% of intervals created in this way contain the true population mean.

D.	If we get another sample, then we can be 95% sure that the mean of this second sample is between 205 and 295.
Ans) Incorrect. The interval doesn’t describe the mean of another sample.

E.	We can be 95% confident that the range 160 to 340 holds the population mean.
Ans) Incorrect. The interval doesn’t correspond to 95% confidence level.


7.	Which is shorter: a 95% z-interval or a 95% t-interval for μ if we know that σ =s?

A.	The z-interval is shorter
B.	The t-interval is shorter
C.	Both are equal
D.	We cannot say


Questions 8 and 9 are based on the following: To prepare a report on the economy, analysts need to estimate the percentage of businesses that plan to hire additional employees in the next 60 days.
Ans) A. the Z-interval is shorter.

8.	How many randomly selected employers (minimum number) must we contact in order to guarantee a margin of error of no more than 4% (at 95% confidence)?

A.	600
B.	400
C.	550
D.	1000
Ans) n=no of employers, Assume p^=0.5, q^=0.5 margin of error=0.04
	For 95% confidence interval, the critical value z=1.96
		ME=Z*sqrt((p^*q^)/n)
		0.04=1.96*sqrt((0.5*0.5)/n)
		N= (1.962*0.5*0.5)/0.042=0.9604/0.0016=600


9.	Suppose we want the above margin of error to be based on a 98% confidence level. What sample size (minimum) must we now use?

A.	1000
B.	757
C.	848
D.	543
Ans) Z=2.576
	0.04=2.326*sqrt((0.5*0.5)/n)
	N= (2.3262*0.5*0.5)/0.042=1.3525/0.0016=845.35



# Assignment set-4
# Topics: Sampling Distributions and Central Limit Theorem


	Examine the following normal Quantile plots carefully. Which of these plots indicates that the data …
	
  ![image](https://user-images.githubusercontent.com/99672298/158005525-53b401f9-b024-413a-84ef-6b80761c8cce.png) \

Are nearly normal?\
Ans => C\
	Have a bimodal distribution? (One way to recognize a bimodal shape is a “gap” in the spacing of adjacent data values.) => B and D\
	Are skewed (i.e. not symmetric)? =>A,B and D\
	Have outliers on both sides of the center? => A and B

 


	For each of the following statements, indicate whether it is True/False. If false, explain why.

The manager of a warehouse monitors the volume of shipments made by the delivery team. The automated tracking system tracks every package as it moves through the facility. A sample of 25 packages are selected and weighed every day. Based on current contracts with customers, the weights should have μ = 22 lbs. and σ = 5 lbs.

	Before using a normal model for the sampling distribution of the average package weights, the manager must confirm that weights of individual packages are normally distributed.
Ans: False 
: A sampling distribution is a probability distribution of a statistic obtained from a larger number of samples drawn from a specific population.
In our case the samples contain 25 packages and the larger number of samples contain of each such 25 packages taken into different samples (25+25+25+25…and so on). The mean for one these samples is 22lbs and standard deviation of 5lbs which means each individual package is having a weight varying between + or – 5lbs with respect to mean(22lbs). Hence it is invalid to take a weight of individual packages and confirm that it follows normal distribution before using a normal model for the sampling distribution. The Sample Central Limit Theorem states that the sampling distribution of the samples mean approaches normal distribution as the sample size is large enough.

	The standard error of the daily average SE(x ̅) = 1.
Ans: True :
 As SE(Standard Error)  =  sample standard deviation / Square root of (number of sample)
SE = 5 / (25)^1/2
SE = 1

	Auditors at a small community bank randomly sample 100 withdrawal transactions made during the week at an ATM machine located near the bank’s main branch. Over the past 2 years, the average withdrawal amount has been $50 with a standard deviation of $40. Since audit investigations are typically expensive, the auditors decide to not initiate further investigations if the mean transaction amount of the sample is between $45 and $55. What is the probability that in any given week, there will be an investigation?

	1.25%
	2.5%
	10.55%
	21.1%
	50%

Ans: D
t=(x-mean)/sigma/sqrt(n); t-test, because standard deviation is not given for the long term
=(45-50) or (55-50)/40/sqrt(100)
=+/- 5/40/sqrt(100)
=+/- 1.25
The probability of z between those values is 0.7857, so probability of an investigation is 1-0.7887, or 0.214.

	The auditors from the above example would like to maintain the probability of investigation to 5%. Which of the following represents the minimum number transactions that they should sample if they do not want to change the thresholds of 45 and 55? Assume that the sample statistics remain unchanged.

	144
	150
	196
	250
	Not enough information
Ans:  D
For 5%, t-value is +/-1.96
t_value = (x_bar – mew)/(sample_standard_deviation/sqrt(n)) 
so 1.96=(5)/(sqrt(n)/40)
sqrt(n)= (40*tvalue)/(5)
n=248 

	An educational startup that helps MBA aspirants write their essays is targeting individuals who have taken GMAT in 2012 and have expressed interest in applying to FT top 20 b-schools. There are 40000 such individuals with an average GMAT score of 720 and a standard deviation of 120. The scores are distributed between 650 and 790 with a very long and thin tail towards the higher end resulting in substantial skewness. Which of the following is likely to be true for randomly chosen samples of aspirants?

	The standard deviation of the scores within any sample will be 120.
	The standard deviation of the mean of across several samples will be 120.
	The mean score in any sample will be 720.
	The average of the mean across several samples will be 720.
	The standard deviation of the mean across several samples will be 0.60
Ans: E 
Standard error = sigma / (n)^0.5
                            = standard deviation / (sample size)^0.5
                            = 120 / (40000)^0.5
                            = 0.6
