[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

#import package

import scipy.stats

#Take the mu and sigma from the problem to create the normal distribution model model.

mu = 178

sigma = 7.7

dist = scipy.stats.norm(loc=mu, scale=sigma)

#convert feet to centimeters and find the percentile. Then subtract in order to find the interval that meets the Blue Man requirements.

shortest =dist.cdf(177.8)

tallest =dist.cdf(185.4)

tallest-shortest
