[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

```python
# Solution goes here
>>>'firsts are {} std deviations different.'.format(CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb))
>>>'firsts are -0.088672927072602 std deviations different.'
```
On average, firsts are roughly the same weight as others, showing that there is about a -.08 standard deviation between the two groups. With this data, we can assume that no more than a random difference between the two.