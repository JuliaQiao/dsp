[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

#Generate 1000 random numbers between 0 and 1.

random = np.random.random(1000)

#create pmf and plot it.
random_pmf = thinkstats2.Pmf(random, label = 'random_pmf')

thinkplot.Pmf(random_pmf)

thinkplot.Config(xlabel = 'Random Number', ylabel = 'Probability')
#pmf shows equal probabilities for all numbers. This means the distribution is uniform.

#create cdf and plot it.
random_cdf = thinkstats2.Cdf(random, label = 'random_cdf')

thinkplot.Cdf(random_cdf)

thinkplot.Config(xlabel = 'Random Number', ylabel= 'Probability')
#cdf is a straight diagonal line, proving that the distribution is indeed uniform.
