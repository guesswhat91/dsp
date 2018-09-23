[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

**I USED THE FUNCTIONS THAT THE AUTHOR PROVIDED IN THE BOOK**  

_'''Importing all the packages that was provided by the author to answer Exercise 2 '''_  
_from __future__ import print_function, division_  

_%matplotlib inline_  

_import numpy as np_  

_import nsfg_  
_import first_  
_import thinkstats2_  
_import thinkplot_  


_'''Generating a set of random numbers using numpy'''_  
_ex_sample = np.random.random(1000)_  

_'''usinf the Pmf class that the author provided in the thinkstats2 package'''_  
_ex_sample_pmf = thinkstats2.Pmf(ex_sample, label='pmf_ex_sample')_  

_'''Using thinplot to plot pmf distribution'''_  
_width = 0.4 / 16_  
_thinkplot.Pmf(ex_sample_pmf, width=width)_  
_thinkplot.Config(xlabel='ex_sample', ylabel='PMF')_  

_'''Using thinplot to plot cdf distribution'''_  
_cdf_ex_sample = ex_sample_  
_thinkplot.Cdf(thinkstats2.Cdf(cdf_ex_sample, label='cdf_ex_sample'))_    
_thinkplot.Config(xlabel='edf_ex_sample', ylabel='CDF')_    

**The cdf distribution is uniform since it uses the 'Cdf'class (that the author provides) where the random numbers are ranked uniformly**  
