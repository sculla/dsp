[Think Stats Chapter 8 Exercise 3](http://greenteapress.com/thinkstats2/html/thinkstats2009.html#toc77)

```python

def test_1(l=2, n=1000):
    simulations = []
    for _ in range(n):
        simulations.append(SimulateGame(l))
    results = 'Results n = {}:\nRMSE L = {:.4f}\nMean error L = {:.4f}\n'\
            .format(n,RMSE(simulations,l),MeanError(simulations,l))
    print(results)
for i in [1e3, 1e6, 1e9]:
    test_1(n=int(i))

```

Results n = 1000:
RMSE L = 1.3989
Mean error L = -0.0070

Results n = 1000000:
RMSE L = 1.4153
Mean error L = 0.0011

Ran out of memory for the 1e9.. trying to figure out a way to batch it by 1e6 elements