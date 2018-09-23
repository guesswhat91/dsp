[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

_import scipy.stats_  

_mu = 178 #avg male height in the U.S._  
_sigma = 7.7 #std deviation for male height of U.S. population_  
_dist = scipy.stats.norm(loc=mu, scale=sigma) creating normal dist using scipy_  

_# Solution goes here_ 
_upper = dist.cdf(185.42) # converting 6'01 to cm_  
_lower = dist.cdf(177.8) # converting 5'10 to cm_  
_rnge = round((upper - lower) *100,0) calculating percent between required blue men height_  
_print(f'About {rnge}% of the U.S. male population are between 5\'10 and 6\'01')_  
