[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

```python
import numpy as np
ran_num = np.array(np.random.random(1000))

pmf = thinkstats2.Pmf(ran_num)
thinkplot.Pmf(pmf)

thinkplot.Cdf(pmf)
```

This shows a weird graph, which is uniform for both the PMF and the CDF values, this is actually confusing to me. I would assume a uniform distribution would show a CDF that is diagonal due to the values being below n, as before, but both plots show a roughly flat plot with an even distribution at .001