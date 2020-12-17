---
layout: post
title: Format labels in plot.ly
image: 
tags: [plot.ly, Dash]
---

If you don't like the default number formatting in hover labels in plot.ly, you can change them using D3.js formatting codes.

```python
layout= go.Layout(
    hovermode= 'closest',
    xaxis= dict(
        title= 'My x axis (shown in thousands instead of 500k)',
        zeroline= False,
        hoverformat=',f'
    ),
    yaxis=dict(
        title='My y axis (shown in % instead of having to *100)',
        hoverformat='.2%%'
    ),
)
```
