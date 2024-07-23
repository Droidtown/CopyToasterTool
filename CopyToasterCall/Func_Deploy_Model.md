# 部署 CopyToaster 模型

> 適用於 CopyToaster 模型

部署 CopyToaster 的模型

```python
from requests import post
from pprint import pprint

url  = "https://api.droidtown.co/CopyToaster/Call/"

payload = {"username": username, # 這裡填入您在 https://api.droidtown.co 使用的帳號 email。
	   "copytoaster_key": key, # 這裡填入您在 https://api.droidtown.co 登入後取得的 copytoaster_key。
	   "func": "deploy_model",
	   "data": {}
}
response = post(url, json=payload).json()
pprint(response)

```

輸出結果如下：

```python
{
"msg": "Success!", 
"status": True
}
```
