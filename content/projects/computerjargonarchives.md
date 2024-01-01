---
title: 'Computerjargon.com Archives'
summary: Historical archive of contents from Computerjargon.com from 1999-2010.
kind: page
---

## Summary

Historical archive of contents from [Computerjargon.com](https://www.computerjargon.com) from 1999-2010.

## Code

Retrieves a list of all snapshots between 1999 and 2010 for [Computerjargon.com](https://www.computerjargon.com) and saves the results to disk.

```python
import os
import requests
import time 
from waybackpy import WaybackMachineCDXServerAPI


url = "http://www.computerjargon.com"
user_agent = "Mozilla/5.0 (Windows NT 5.1; rv:40.0) Gecko/20100101 Firefox/39.0"
output_path='output/computerjargon/{0}.html'

cdx = WaybackMachineCDXServerAPI(url, user_agent, start_timestamp=1999, end_timestamp=2010)
for item in cdx.snapshots():
    if not os.path.exists(output_path.format(item.timestamp)):
        # Purposefully moved the request before opening the file because of rate limiting on the wayback machine
        content = requests.get(item.archive_url).content
        with open(output_path.format(item.timestamp), 'wb') as f:
                f.write(content)
        time.sleep(10)
```

## Archives

{{< directorylist path="static/projects/computerjargonarchives/" >}}