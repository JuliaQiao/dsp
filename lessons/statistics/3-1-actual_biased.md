[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

#setting up the dataframe I need from the dataset
resp = nsfg.ReadFemResp()

#creating a pmf using the provided respondent variable label and labeling it.
pmf = thinkstats2.Pmf(resp.numkdhh, label='numkdhh')

#plotting the pmf, with x-axis labeled for 'Number of Children' and y-axis labeled for 'Probability'
thinkplot.pmf(pmf)
thinkplot.Config(xlabel = 'Number of Children', ylabel = 'Probability')

#using the provided BiasPMF function which takes a pmf and creates a biased one by making a copy of it, to create a biased pmf.
biased = BiasPmf(pmf, label = 'biased')

#plotting the original pmf and biased pmf 
thinkplot.PrePlot(2)
thinkplot.pmfs([pmf,biased])
thinkplot.Config(xlabel= 'Number of Children', ylabel= 'Probability' )
#we see that the biased distribution has more children than the original one--starting for 2 children and larger. The observations for 1 child remains the same between the two, while 0 children has no observations in the biased pmf but actually account for the most observations in the original pmf.

#calculate the means of each pmf
pmf.Mean()
#1.024205155043831
biased.Mean()
#2.403679100664282

#the biased pmf mean is more than twice that of the original.

