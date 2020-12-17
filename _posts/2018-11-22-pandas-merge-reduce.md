---
layout: post
title: Building a dataframe with reduce and a list comprehension
image: 
tags: [Python, pandas]
---

I am unreasonably pleased with this code snippet.

I'm building a dataframe for ML from a series of queries to different databases. Each function has the same input arguments, and outputs a dataframe with an identically labelled primary key for merging.

Instead of sequentially merging each dataframe and building it up stepwise, I use `reduce` and a list comprehension.

Remember that
`reduce(lambda x, y: x+y, [1, 2, 3, 4, 5])`
 calculates ((((1+2)+3)+4)+5).

So, I can write

```python
from functools import reduce

functions = [function1, function2, function3, function4,
             function5]

combined_df = reduce(lambda left, right:
                    pd.merge(left, right, on=['primary_id', 'year']),
                    [f(arg1='abc', arg2='123') for f in functions])
```

to create my merged dataframe in two lines.
