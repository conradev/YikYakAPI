# Yik Yak API

This is a Python implementation of the private Yik Yak API.

## Example

``` python
from yikyak import YikYakAPI

yyapi = YikYakAPI(None, 37.427367, -122.169982)
yyapi.registerUser()
messageID = yyapi.sendMessage('test').get('yakID', None)

for x in range (0, 140):
	yyapi = YikYakAPI(None, 0, 0)
	yyapi.registerUser()
	print yyapi.likeMessage(messageID)
```