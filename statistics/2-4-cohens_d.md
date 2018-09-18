[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

_**#My pyhton code to see if first babies are lighter.**_

from __future__ import print_function, division #used this from the book. 

%matplotlib inline #used this from the book. 

import numpy as np #used this from the book. 

import nsfg #used this from the book. 
import first #used this from the book. 


firsts = live[live.birthord == 1] #used this from the book. 
others = live[live.birthord != 1] #used this from the book.  

if firsts.mean().totalwgt_lb < others.mean().totalwgt_lb:  
    print("First Babies are lighter than others")  
else:  
    print("First Babies are heavier that others")  
    
firsts.mean().totalwgt_lb, others.mean().totalwgt_lb  

**_I used the same fucntion that the author provided in the book**_. 

_def CohenEffectSize(group1, group2):  
    """Computes Cohen's effect size for two groups.
    
   _group1: Series or DataFrame_
    _group2: Series or DataFrame_
    
   _returns: float if the arguments are Series;_ 
             _Series if the arguments are DataFrames_
   """
    _diff = group1.mean() - group2.mean()_

   _var1 = group1.var()_
   _var2 = group2.var()_
   _n1, n2 = len(group1), len(group2)_

   _pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)_
   _d = diff / np.sqrt(pooled_var)_
   _return d_


CohenEffectSize(firsts,others).totalwgt_lb

-0.088672927072602


