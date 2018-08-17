---
layout: post
title: Formatting print output in Python 3.7
image: 
tags: [Python]
---

Here's a new trick for formatting output in Python 3.7 I didn't know.

Before you could write

```
In [1]: something = 'Test variable'

In [2]: print('This is my {0}.'.format(something))
This is my Test variable.
```

But now you can also write

```
In [3]: print(f'This is my {something}.')
This is my Test variable.
```

with the ```f``` at the start of the print statement.
