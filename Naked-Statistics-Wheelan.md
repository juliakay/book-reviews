# Naked Statistics by Charles Wheelan - Notes, Summary, and Some Additional Thoughts

##### Table of Contents  
[Chapter 1](#chapter1)  
[Chapter 2](#chapter2)  
[Chapter 3](#chapter3)  
[Chapter 4](#chapter4)  
[Chapter 5](#chapter5)  
[Chapter 5.5](#chapter5.5)     
[Chapter 6](#chapter6)  
[Chapter 7](#chapter7)  
[Chapter 8](#chapter8)  
[Chapter 9](#chapter9)  
[Chapter 10](#chapter10)  
[Chapter 11](#chapter11)  
[Chapter 12](#chapter12)  
[Chapter 13](#chapter13)  

## Introduction 
"The point of this book is to make the most important statistical concepts more intuitive and more acessible"   

"It's easy to lie with statistics, but it's hard to tell the truth without them" - Andrejs Dunkels  

<a name="chapter1"/>

## Chapter 1: What's the Point?

>Statistics is a handy tool for collapsing complex information into a single number. It has no intrinsic meaning, but a rather a tool for comparison.   

- To summarize huge quantities of data  
- To make better decisions  
- To answer important social questions  
- To recognize patterns that can refine how we do everything from selling diapers to catching criminials    
- To catch cheaters and prosecute criminals 
- To evaluate the effectiveness of policies, programs, drugs, medical procedures and other innovations  

**Fun fact:** The US has a Gini index (a measure of wealth distribution on a scale of 0 to 1, 0 being identical wealth) of 0.45. China is .42. Sweden is .23. Canada is 0.32. Brazil 0.54. South Africa 0.65.   

Statistics help us process data, which is really just a fancy name for *information* - whether that infromation be trivial or insightful.

**1. Descriptive Statistics**
- We use descriptive statistics everyday (sports, GPA, etc). Descriptive statistics exist to **simplify**, which always implies some loss of nuance or detail. Anyone working with numbers needs to recognize as such.

**2. Inference**
- Using data from the "known world" to make informaed inferences and conjecturs about the "unknown world". This is where sampling can come in.

**3. Asessing Risk and Other Probability-Related Events**
- Why do casinos "always" win? 
    - Casinos are not making money at any given moment, but are making money in the long-run. This is because the underlying probabilites of each event (drawing 21 in blackjack or landing on red in roulette) is known - and these probabilities always favor the house.  
    - This also hinges on the Law of Large Numbers. See [Chapter 5](#chapter5)  
- All risk models have probability at it's foundation. Casinos, business, the 2008 crisis, insurance etc. We usually can not make these risks ever go away, but we can engineer cheats to protect ourselves ( i.e. charging premiums, building fences, installing fire detectors).  

**4. Identifying Important Relationships (Statistical Detective Work)**
- Optimal conditions for testing usually do no exist - so we turn to scientific inference instead. The data present unorganized clues - wehre we must work to craft the raw data into some meaningful conclusion.  
- Typical Inference Flow:
    1. What is the association between x and y variables (controlling for other factors that may affect the result)
    2. What is the likelihood that the association between x and y is merely a coincidence
- Typically we can isolate a strong assocaition between variables, but can not necessarily explain WHY. 
    - But that's okay and not something that should be discouraging. In fact, its important to focus less on the technicallities of statistics and focus more on learning insights that inform our lives. 

**5. Lies, Damned Lies, and Statistics**
- Statistics typically builds cases on imperfect data. There are limits on the data we can gather and the kinds of experiments we can perform.  
- At the end of the day we must conduct analysis using the best data and methodologies and resources available. 

<a name="chapter2"/>

## Chapter 2: Descriptive Statistics - Who was the beest baseball player of all time?

Descriptive Statisics are just a "sumamary" statistic often used to compare two or more things.

When given a large set of data, was is typically a good first step? Find the "middle" statistics - the "central tendancy". 

Helpful Metrics:
- Mean : Often skewed by outliers
- Median
    - Quartiles
- Standard Dev
    - Variance: sqrt (stdev) - a measure of how far from mean - rarely used as a descriptive statistic

The Normal Distribution:
- Data that is distributed normally in a bell shape around it's meam

Perventage change vs percentage. Change in rate vs rate difference.
    - Know and mind the differences 

<a name="chapter3"/>

## Chapter 3: Deceptive Description - He's got a great personality!

- Accuracy vs Precision
    - Precision is "exactness" not correctness
    - Accuracy is correctness
    - If any answer is accurate, then more precision is usually better, but no amount of preicsion cam make up for inaccuracy 
    - BUT exactness and specificy can cause a false sense of credibility - so be careful 
    - How does this relate to statistics?
        - Wrong assumtopins can give us precision math but totally miss the point of exactly what we are trying to define, describe or explain.

This isnt mentioned in the chapter, but I think it is a good technical concept that captures what this chapter is about: 
- **Simpsons Paradox** :  in which a trend appears in several different groups of data but disappears or reverses when these groups are combined (wikipedia). Aka Thing 1 can be better and worse, greater and less than, increasing and decreasing compared to Thing 2.
    - Why does this happen?
        - This often happens with percentages, which hides the sample size. Typically one sample size is significantly greater than the other.  
        - Example:
            ![Simpsons](https://miro.medium.com/max/1400/1*l-F5-80NqgsGiDk2I4Z0Ew.png)

Pretty Cool Stuff

<a name="chapter4"/>

## Chapter 4: Correlation - How does Netflix know what movies I like?

*Correlation* measures the degree to which two phenomena are related to one another. The power of correlation as a statistial tool is that we can encapsulate an association between two variables ina single descriptive statistic: *the correlation coefficient*. The value will range from -1 to 1 and has no unit (which is a good thing! less complexity is good).

How its calculated - intuitively:
1. Calculate the mean and the std dev for the two variables you are comparing
2. Convert each variable as a measure of std dev from the mean (and don't forget the proper sign)
3. Take the product of moth std dev measurements
4. Sum all products and divide by number of opervations
If the two variables tend to deviate from the mean in any meaningful pattern than we have a correlation!
- Formula:
    ![CorrelationCoef](https://lh3.googleusercontent.com/proxy/O6Et7Hnti-XCdwa95XA8Zdt8axsGChHS6-yQzN8YwTgkQE5qhkqGI_9VgfjrH52lXlM78tnphcoCyk39Sfoxbw13vpke08B1O2uw9Q)

**Fun Fact**: SAT and college performance have a correlation of 0.54. High school GPA and college performance have a correlation of 0.54. But High School GPA combined with SAT have a 0.64 correlation with college performance.

Just keep in mind that correlation does not imply causation 

Regarding Netflix question - an over simplified explanation: 
- You rate films and Netflix has a sample of films you like
- Netflix takes your data and finds a handful of other users that like the same thing aka have high positive correlation with
- Netflix reommends films that similar people rated highly that you have not watched yet

<a name="chapter5"/>

## Chapter 5: Basic Probability - Don't buy the extended warranty on your $99 printer

**Probability** is the study of events and outcomes involving an element of uncertainty.
- It can tell us what is likely to happen and what is less likely to happen
- It can also sometimes tell us after the fact what likely happened and what likely did not happen

Example: CSI DNA match
- Saliva is found on an apple core and we extract the DNA
- It looks something like _234__23_576_8_97___5_6
- 2*234*76*23*6*576*7*8*4*97*808*5*0*6* is someones DNA - we have a match!
- This is where probability comes in, what are the odds that this is the wrong person and that the match was purely by chance
- The more samples, data, and time we have - the more certina we can become

Probability of multiple events
- If two events are independent
    - P(A and B) = P(A) * P(B)  
    - P(A or B) = P(A) + P(B)  
- Expected Value - useful in finance, determining "fairness", finding the value of something, total payouts/costs etc
    - To help visualize think of probability tree. Each branch split should always add back up to 100%

Law of Large Numbers
- Given any number of trials, the outcome will always converge around the expected value which will look like a bell curve
- As the number of trials increase, the outcomes strongy aggregate around the EV and the probability of getting something outside of the EV falls sharply. This will graph will have a very point middle

So why no warrranty on printer? 
Because insurance companies make money off statistics. The cost of the warranty will always be greater than the expected value of the loss. On average, you would have to pay morer for the warranty than to fix it. The only reason to buy insurance is to avoid any large/sudden costs that you cannot comfortably afford to withstand.   
So with that said, billionaries should never buy insurance because they should be able to afford anything that might happen to them. Not buying insurance would actually save them money!

<a name="chapter5.5"/>

## Chapter 5.5: The Monty Hall Problem

what is the Monty Hall Problem? 
- There are three doors. One of which has a prize, the other two have a goat
- If you pick the door with the prize you win!
- Once you pick a door, one of the other two doors that does not contain the prize will be revealed
- You are then given the option to switch your choice of door. **Do you switch doors?**
    - If you switch you have a 2/3 chance of winning
    - If you don't switch, you have a 1/2 chance of winning

Why is it 2/3 instead of 1/3 if he switches?
- Because Monty knows which door has the prize. So by switvhing we get the benefit of choosing two doors rather than one
- It's the equivalent of being asked, *would you like to switch your choice for both of the other doors you did not choose?*
    - To this you should say yes because 2 doors > 1 door

Makes sense why this show isn't still going on - 2 out of 3 contestants would have walked away with very big prizes after revealing that stats behind it.

<a name="chapter6"/>

## Chapter 6: Problems with Probability - How overconfident math geeks nearly destroyed the global financial system

Imagine having an airbag that works 99% of the time - an airbag that works all the time, except when you have a car accident. LOL

2008 Financial Crisis was driven by 3 main errors:
1. Confusing precision with accuracy
    - like a ruler set to inches instead of cm when you were expecting cm, exact and wrong
2. The estimated and assunmptions of the underlying probabilites were wrong
    - Past events don't always predict future events, especially in the market
3. They neglected their "tail risk", , the small risk of some catastrophic outcome.
    - Focusinig on the 99% upside and not the potential 1% catastrophe

Tips:
- Understanding when events ARE and ARE NOT independent
- Streaks and anomolies happen, it's instinct to assume something besides randomness caused it. But its's probably just randomness
- Most thing will revert back to the mean
    - May contradict "gambler's fallacy" at first glance - but this say the next event is more likely, but rather with more trials the over all avg will move towards the mean
- Statistics vs Discrimination - a hot topic, just don't forget the social implications

<a name="chapter7"/>

## Chapter 7: The Importance of Data - Garbage in, garbage out

3 Things we demand of data:
1. The data sample is representative of some larger group or population
    - a representative sample is the most powerful thing
    - It's harder than it looks
    - Good methods, applied to bad samples are way too common (and this is bad)
    - Size matters, the bigger the better
2. The data provides some source of comparison
    - Test vs control groups
    - Reaching perfect control scenarios are hard, but we can often rely on probability and randomization to help divide the groups
3. Collect data just because you can, becaues you never know when you might need igt

Selection Bias
- Self explanatory - Gathering our data from only a subset of the population
- Control and test groups should also not always be directly compared, since implications for why someone was in a certain group may exist
- Self Selection Bias

Publication Bias
- Positive findings are more likely to be published than negative findings
    - Negative: Video games *do not* prevent colon cancer
    - Positive: Video games *do* lower the incidence of colon cancer
    - Be careful, because sometimes the positive study may have occured by chance and gets published regardless

Recall Bias
- This is occurs when we as a sample to recall their past, rather than collecting ourselves X years ago. Often times they will recall a memory that is exaggerated

Surviorship Bias
- This occurs when some or mamy of the observations are falling out of the sample, changing the composition of the sample
- This is often how mutual fund companies advertise their funds, but closing or folding poor performing funds into other ones

Healthy User Bias
- This comes from the idea that people who faithfully engage in activities and habits that are godo for them, are fundamentally different from those who don't

<a name="chapter8"/>

## Chapter 8: The Central Limit Theorem - The Lebron James of statistics

The central limit Theorem leverages probability and proper sampling - using a sample to make inferences about a large population.
 - A large, properly drawn sample will resemble the population fron with it is drawn
 - In fact, the probability that any sample will deviate massively from the underlying population is very low

 The CLT allows us to go backwards and forwards (from populat to sample, and vice versa)
 1. If we have detailed information about some population, the we can make powerful inferences about any properly drawn sample. (We can expect them to behave the same)
 2. If we have detailed information about some properly drawn sample, we can make strikingly accurate inferences about the popluation from which the sample was drawn.
 3. If we have detailfed information about **both** the sample population and the total population, we can calculate the probability of that particular sample getting drawn from a given population. ( i.e. If this probability is low, we can conclude with high confidence that the sample is actually not drawn from the population)
 4. If we have information about 2+ samples only, we can infer whether or not both samples were likely drawn from the same population.
    
Understanding confidence intervals, hypothesis, standard error and marathon buses 
- approx 99 out of 100 times, the mean of any randomly selected sample will be within 1 standard deviation of the entire population
- if the sample mean is -/+ 1 std dev greater than the pop. mean, that means we can reject the hypothesis that the sample is from the population with 99% certainty
    - also means we'll be wrong 1% of the time ;)
- **Sample means for any population will be distributed roughly as a normal distribution around the population mean**
    - quick refresher:
        - 68% within -/+ 1 standard deviation
        - 95% within -/+ 2 standard deviation
    - the original population does not even need to have a normal distribution for its sample means to be normally distributed
    - sample size n > 30 **
- **Standard Error** is the finishing touch. It will tell us the dispersion of the sample mean aka how tight the samples means will cluster aroudn the population mean.
    - NOT to be confused with Standard Deviation
        - Standard Deviation: measures dispersion in the underlying population
        - Standard Error: measures dispersion of *the sample means*. It is the std dev of the sample means!
            - Formula for SE = std dev / sqrt(n)
                - where n is the size of the sample
    - Using CLT we know that 68% of sample means will be within 1 SE, 95% within 2 SE, 99.7% within 3 SE, etc

Summary:
- Proper samples will resemble the population they come from
- Sample means will be relatively close to that of the popluation, Standard Error will tell us "how close"
- It is unlikely that a sample mean will lie more than 2 standard errors from the population mean   

<a name="chapter9"/>

## Chapter 9: Inference - Why my statistics professor thought I might have cheated

**Hypothesis Testing** - USing statistical inferences to accept or reject explanations on the basis of their likelihood.
    - All hypothesis testing must start with a null hypothesis. This is often created in hopes of being rejected
    - *Hypothesis testing shows correlation, but not causation*
    - hypothesis testing and statistical signifcance can be decieving when it comes to actually *size* of the difference between test and control

How we argue to reject the null:
1. If the null were true, we would rarely see this amount of variation in outcomes between test and control groups
2. Therefore, if it highly unlikely that the null is true
3. So finally, an alternative - and more likely - explanation for the pattern of data observed is the alternative hypothesis 


What happens when we dont reject the null:
- Often times this strictly means we have *failed to reject* our null hypothesis, we did not *prove* the null hypothesis to be true
- The judgement and position of whoever is reading the experiment can then decide how to interpret it
- Example: Test cheating scandal
    - We observed that the number of answer changes from wrong to right in the last 10 mins are 20-50 std dev above norm
    - With such high std dev, we can reject the null hypothesis that these results were legitimate
    - *But they could not prove that cheating was going on*, but using our judgement we can assume they cheated

When to reject the null:
- If the null hypotehsis is true, how likely is it that we would observe this pattern of data by chance?
- a probability of 0.05 or 5% is the most common thresohold for significant level
    - if the chance of what happened (given that the null is true) is less than 5%
    - if the mean of the sample is true mean +/- 2 std error, then we can reject the null
- When we can reject a null hypothesis at some reasonable significance level, the results are said to be **statistically significant**
- **p-value** is the *specific* probability of getting a result at least as extreme as the one you've observed if the null hypothesis is true
    - if we reject the null, that means the probability of what we observed would happen at less than 5%. The p-value should tell us exactly how probable the even will happen

Hypothesis Testing: Comparing two groups - We can calculate the probability of observing a difference of means at least this large (between two groups)
- Intuition:
    - If we drew two samples from the same population, we would expect the difference between the two sample means to be zero
    - We can calculate the standard error expected between two sample means, a measure of the dispersion we can expect
    - Using this standard error metric, we can calculate the probability that two samples come from the same population
- What we know from CLT:
    - CLT tells us sample means will follow the normal distribution
    - If two samples come from the same population, the difference between their means will be within 1 **standard error** of zero 68% of the time
        - the difference between their means will be within 2 standard error of zero 95% of the time
    - This standard error is calculated like so:
    ![Standard Error](https://sphweb.bumc.bu.edu/otlt/MPH-Modules/BS/SAS/SAS5-Comparing2IndependentMeans/Equation13.png)
    - where S is the standard DEVIATION of the POPULATION

**Type I:** False Positive  
**Type II:** False Negative

One- and Two- Tailed Hypothesis Testing
- Depending on how many tails, our cutoff point ofr rejecting our null hypothesis will be different
- Two- Tailed: we account for large difference in means in both directions: positive and negative 
    - If using a 5% significance level, that means we will allow for 2.5% probability on both ends
- One- Tailed: We account for a large difference in means in one direction: greater or less than
    - If using a 5% significance level, we will have all 5% wiggle room in one tail

<a name="chapter10"/>

## Chapter 10: Polling - How we know that 64% of Americans support the death penalty (with a sampling error +/- 3%) 

A **Poll** is an inference about the opinions of some population that is biased on the views expressed by some sample drawmn from that population.
- Stems from the Central Limit Theorem, if we take a large enough, representative sample we can assume that our sample will look a lot like the population from which it is drawn

Polls vs other samples:
- Polls will have a sample statistic thatis a percentage or proportion
- Others forms of samples may use a mean

when the sample satistic is a percentage:
- the standard error is slightly different
    - sqrt(p(1-p)/n)
        - p = proportion of respondents expressing a particular view
        - as n increases, the standard error will decrease
        - error will be smaller if the "p"s are further apart, more different

Example: Election results:
- Repub: 53%, Dem: 45%, Ind: 2%
- Standard Error (using repub candidate as proportion of interest) = 2%
- we can be 68% sure with a margin of error of 2%
- we can be 95% sure with a margin of error of 4%
    - this puts Repub: [49%,57%] and Dem: [41%, 49%]
    - So there might be a tie...is there anything we can do (without more data)? Nope, other than just give a more timid and vague conclusion
    - if we had more data, even if it was similar in results, by increasing n we could potentially decrease the standard error giving us a better answer
- Technically each group will have its own standard error, but in practice it is common to go with the SE that is higher in value

Tips for Polling
- Is this an accurate sample of the population?
    - watch out for low response rates and volunteers. This can lead to samplng bias
- Have the questions been posed in a way that elicits accurate information on the top of interest?
- Are respondents telling the truth?

Not sure when I will ever use polling...but still good to know!

<a name="chapter11"/>

## Chapter 11: Regression Analysis - The miracle elixir

**Regression Analysis** allows us to quantify the relationship between a particular varriable and an outcome that we care about *while controling other factors*.
- In other words, isolating the effect of one varirable while holding the effects of the other variables constant
- Regression will also only give us an estimate
- Regression is powerful in that is allows us to unravel complex relationships in which multiple factors affect some outcome that we care about
    - Giving us an estimate of *each* explanatory variable and the dependent variable while holding other dependent variables constant
- This becomes increasing valuable when we are unable to do controlled experiments on people

What is needed for Regression:
- Similar to polling, we need a good and representative sample

- Example: Exercise and Disease
    - We see results that people who exercise 3-4 times a week have sharply lower rates of heart disease than people who don't exercise
    - We can say we see an association between exercise and heart disease. 
    - It is NOT to tell nonexercisers who are sick that they should have exercised
    - We are NOT proving definitively that exercise prevents hearts disease
    - We are only rejecting the null hypothesis that exercise has no association with heart disease

Simply put, the slope of the line (the regression coeff) will tell is the direct impact of one dependent variable and our variable of interest
- when looking at the regression coeff, considerr its Sign, Size and Significance
- Standard Error and Reg Coeff
    - We can also computer the standard error of the coeff and see how it changes if we were to resample and rerun our regression
    - Sample size matters here:
        - Large sample : follow normal distribution
        - Small sample : follow t-distribution (flatter and fatter tails / more dispersed)
            - The t-distribution will vary depending on how many degrees of freedom we have. As df approaches infinity, the t-distribution will become the normal distribution
            - That means the underlying probabilities will also change (vs normal distribution)
            - Using the t-distribution and t-statistic
                - calcualte the t-statistic = coeff/ standard error
                - evaluate t-statistic against the appropriate t-distribution
                - when t-statistic is large, that means our observed coeff is far from what the null would predict (usually 0), and we can reject the null
            - the fewer degrees of freedon (smaller sample), the larger the t-statistic would have to be for us to reject the null

Regression and Hypothesis testing:
- Often times the null hypothesis says that the regression coefficient is zero (no relationship)
- 95% of our sample will have a coeff that is reg coeff +/- (2 * std error)
    - if 0 is not in our interval, we can reject the null
- Rule of thumb, if the coefficient is at least twice the size of the standard error, it is likely to be statistically significant
    - The ratio of the standard error : coefficient is call the **t-statistic**


**R^2 Statisic** tells us the total amount of variable explained by the regression equation
- If R^2 Statistic is .25 or 25%, that means 75% of the data is unexplained and that there are other factors that influence our variable
- As we add more variables, the regression will calculate it so to minimize the total sum of the squared residuls for the regression equation

What happens when we add features to our regression:
- As we add all the coeff will adjust accordingly
- Make sure all the coeff are still statistically significant 
- Hopefully R^2 will also increase

<a name="chapter12"/>

## Chapter 12: Common Regression Mistakes - The mandatory warning label

7 Common Mistakes

1. Using regression to analyze a nonlinear relationship
2. Correlation does not equal causation
3. Reverse causality
    - An association between A and B does not prove A causes B. In fact, it is possible that B is causing A.
4. Omitted variable bias
    - Don't exclude important explanatory variables
5. Highly correlated explanatory variables (multicollinearity)
`   - This happens when 2+ variables are essentally "overlap" and we can not isolate the effect of on on the dependent variable
    - To account for this, either use just 1 of the varibles or create a new composite variable that accounts for all of them
6. Extrapolating beyond the data
    - Our results are valid only for a population that is similar to the sample on which the analysis has been done
7. Data mining (too many variables)
    - This about the coin flip scenario where someone flips tails 5 times in a row. We know it's just luck, of often times we look into irrelevant details like "technique", outfit, age, gender, etc which is all irrelevant and misleading

TL;DR:
- Think logically about what variables should be included, what might be missing, and how the results can/should be interpreted
- Regression points is in the right direction, but is rarely enough to prove anything

<a name="chapter13"/>

## Chapter 13: Program Evaluation - Will going to Harvard change your life?