[Think Stats Chapter 6 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2007.html#toc60) (household income)

```python

import math

def RawMoment(xs, k):
    return sum(x**k for x in xs) / len(xs)
def Median(xs):
    cdf = thinkstats2.Cdf(xs)
    return cdf.Value(0.5)
def Mean(xs):
    return RawMoment(xs, 1)
print(Mean(sample), Median(sample))
```  
4.949920244429583 The sample is skewed left.  

```python
def PearsonMedianSkewness(xs):
    median = Median(xs)
    mean = RawMoment(xs, 1)
    var = CentralMoment(xs, 2)
    std = math.sqrt(var)
    gp = 3 * (mean - median) / std
    return gp
print(PearsonMedianSkewness(sample), 'This also shows a positive Skewed-ness, to the left.')
```  
0.7361258019141782 This also shows a positive Skewed-ness, to the left.


```python
m = Mean(sample)
'{:.2%} of households are below mean income of ${:,.2f}'.format(cdf.Prob(m), m)
```

'66.00% of households are below mean income of $74,278.71'