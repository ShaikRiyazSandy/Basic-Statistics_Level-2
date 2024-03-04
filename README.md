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
# Assignment set-4
