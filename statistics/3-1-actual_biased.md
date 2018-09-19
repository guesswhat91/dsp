[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

**I USED THE FUNCTIONS THAT THE AUTHOR PROVIDED**  

_#Importing all the packages._   
from __future__ import print_function, division  

%matplotlib inline  

import numpy as np  

import nsfg  
import first  
import thinkstats2  
import thinkplot  

_#Definng the Respondent data (from nsfg) as a variable_.  
resp = nsfg.ReadFemResp()  

_#from the respondent dataframe defining the 'numkdhh' as a variable_.  
d = resp.numkdhh 

_#From the 'thinkstats2' package defining the probability mass function_. 
pmf = thinkstats2.Pmf(d, label='actual') 

_#Getting the mean for the probability mass function for number of children under 18 in respondents houselhold_. 
pmf.Mean()  

_#Defining the biased probability mass function using the 'BiasPmf' function that was provided by the author_. 
biased_pmf = BiasPmf(pmf,label='biased')  

_#Plotting the two distributions_. 
thinkplot.PrePlot(2)  
thinkplot.PrePlot(2)  
thinkplot.Pmfs([pmf, biased_pmf])  
thinkplot.Config(xlabel='Class size', ylabel='PMF')  

_#Getting the means for both distributions_. 
print('Actual = ', pmf.Mean())  
print('Biased = ', biased_pmf.Mean())  

**In this chapter for the most part everything made sense. Where I had some questions on how the Bias and Unbiased distribution was calculated:**  
1. _In the bias function that the author **multiplies** the class size by the probability of number of students who observe the that class. Is this the norm to crete an unbiased distribution?_. 
2. _In the unbiased function the author **divides** the class size by the probability of number of students who observe the that class_.  


