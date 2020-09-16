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

My output was negative, but Cohen's D is interpreted as an absolute number. this is much higher than 0.029 --the difference in pregnancy length. However, it's still low and doesn't look statistically significant.
