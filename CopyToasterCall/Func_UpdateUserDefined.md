# 建立 CopyToaster 的 userDefined

> 適用於 CopyToaster 模型

在 CopyToaster 中建立 userDefined


## Docker 版

```python
from requests import post
from pprint import pprint

url  = "https://api.droidtown.co/CopyToaster/Call/"

payload = {
       "project": project,
	   "func": "update_userdefined",
	   "data": {
            "user_defined": userDefinedDICT
       }
}

response = post(url, json=payload).json()
pprint(response)
```