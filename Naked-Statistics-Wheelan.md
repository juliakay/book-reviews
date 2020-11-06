# Naked Statistics by Charles Wheelan

##### Table of Contents  
[Chapter 1](#chapter1)  
[Chapter 2](#chapter2)  
[Chapter 3](#chapter3)  
[Chapter 4](#chapter4)  
[Chapter 5](#chapter5)      

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

## Chapter 5: Correlation - How does Netflix know what movies I like?