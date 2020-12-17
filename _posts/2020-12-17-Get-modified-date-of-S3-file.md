---
layout: post
title: Get the modified date of an S3 file
image: 
tags: [AWS, TIL]
---

To get the modified date of an S3 file:

```python
import boto3
 
def get_file_modified_date(bucket, key):
    s3 = boto3.resource("s3")
    summaryDetails = s3.ObjectSummary(bucket, key)
    timeFormat = summaryDetails.last_modified
    formattedTime = timeFormat.strftime("%Y-%m-%d")
    return formattedTime
```