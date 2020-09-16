[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

Code: 

#using function 

CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)

\#calculating on my own 

mean_diff = firsts.totalwgt_lb.mean()- others.totalwgt_lb.mean() 

firsts_len = len(firsts.totalwgt_lb) 

others_len = len(others.totalwgt_lb) 

firsts_var = firsts.totalwgt_lb.var() 

others_var = others.totalwgt_lb.var() 

pooled_var = (firsts_len*firsts_var + others_len*others_var)/(firsts_len+others_len) 

cohens_d = mean_diff/np.sqrt(pooled_var) cohens_d

Answer: -0.088672927072602

0.089, in absolute terms, is larger than 0.029 (pregnancy length) but still low when thinking about the context. This means that there is a 0.089 difference in the standard deviation between the means of the two groups (the mean of the first babies being smaller than other babies). Given the textbook example of there being a 1.7 standard deviations difference between male and female heights--a great example of a significant difference, I have to conclude that 0.089 is simply too low to be significant in this context.
