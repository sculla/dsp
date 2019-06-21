[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

```python
import numpy as np
ran_num = np.array(np.random.random(1000))

pmf = thinkstats2.Pmf(ran_num)
thinkplot.Pmf(pmf)

cdf = thinkstats2.Cdf(ran_num)
thinkplot.Cdf(cdf)
```

These graphs show the expected behavior, with a uniform distribution the PMF, and the CDF raises uniformly on the diagonal of the graph, analogous to a plot of y=x.