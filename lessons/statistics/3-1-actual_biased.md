[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

```python
pmf = thinkstats2.Pmf(resp['numkdhh'], label='actual')
biased_pmf = BiasPmf(pmf, label='observed')
thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, biased_pmf])
thinkplot.Config(xlabel='Children above 18 in HH', ylabel='PMF')
print('Unbiased mean', pmf.Mean())
print('Biased mean', biased_pmf.Mean())

```
Unbiased mean 1.024205155043831

Biased mean 2.403679100664282