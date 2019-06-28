[Think Stats Chapter 8 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2009.html#toc77) (scoring)

> I took a few parts from the solution, mainly the vertical lines for the graph to make it look nicer, and be easier to read.

```python
def test_1(n= 10, lam= 2, iters= 1000):
    
    def VertLine(x, y=1):
        thinkplot.Plot([x, x], [0, y], color='0.8', linewidth=3)
    
    means = []
    
    for _ in range(iters):
        xs = np.random.exponential(1.0/lam, n)
        L = 1 / np.mean(xs)
        means.append(L)
    cdf = thinkstats2.Cdf(means)
    thinkplot.cdf(cdf)
    
    stderr = RMSE(means, lam)
    print('standard error', stderr, '  ')
    
    ci = cdf.Percentile(5), cdf.Percentile(95)
    print('confidence interval', ci,'  ')
    VertLine(ci[0])
    VertLine(ci[1])

for i in [3, 10, 100, 1000]:
    print('n={}  '.format(i))
    test_1(n= i)
    print('  \n', end='')
````
n=3  
standard error 2.8232918161730507   
confidence interval (0.9418029830701925, 7.092994983277239)   
  
n=10  
standard error 0.8364685791127595   
confidence interval (1.2492321644261226, 3.7452366934033368)   
  
n=100  
standard error 0.21544492365186302   
confidence interval (1.7060184662877274, 2.412960372282922)   
  
n=1000  
standard error 0.06199602587144626   
confidence interval (1.9037205485775555, 2.1037960082266665)   