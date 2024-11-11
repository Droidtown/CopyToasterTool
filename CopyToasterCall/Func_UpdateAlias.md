# 建立 CopyToaster 的 alias

> 適用於 CopyToaster 模型

在 CopyToaster 中建立 alias


## Docker 版

```python
from requests import post
from pprint import pprint

url  = "https://api.droidtown.co/CopyToaster/Call/"

payload = {
       "project": project,
	   "func": "update_alias",
	   "data": {
            "alias": alias
       }
}

response = post(url, json=payload).json()
pprint(response)
```