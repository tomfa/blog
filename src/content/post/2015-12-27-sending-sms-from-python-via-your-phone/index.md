---
title: "Sending SMS from python via your phone"
pubDate: 2015-12-27
heroImage: /images/markus-winkler-8cP_6sC7Hhw-unsplash.jpg
tags: ["python", "twilio", "pushbullet"]
category: guide
---

Sending SMS using [twilio.com](http://twilio.com) is nice, but it also costs money. If you want something free that you can use for your hobby projects, check out [pushbullet.com](https://www.pushbullet.com/). If you sign up (it's free), you can push SMS with the following:

1.  Sign up at [pushbullet.com](https://www.pushbullet.com)
2.  Get the app
3.  Install pushbullet with pip:
    ```
    pip install pushbullet.py
    ```
4.  Find your API key [here](https://www.pushbullet.com/#settings/account)
5.  Run the code below (replace key)

```python
from pushbullet import Pushbullet

key = 'MyLongAndSillyCoolAPIKey'
pb = Pushbullet(key)

# Depending on your devices, might be device[1] or similar.
phone = pb.devices[0]
pb.push(phone, "+4712345678", "Test message")
```
