# 建立新的 CopyToaster 專案

> 適用於 `CopytToaster` 的模型

在 CopyToaster 中建立一個新的專案 (finance)

```python
from requests import post
from pprint import pprint

url  = "https://api.droidtown.co/CopyToaster/Call/"

payload = {
	"username": username, # 這裡填入您在 https://api.droidtown.co 使用的帳號 email。
	"func": "create_project", 
	"data": {
		"name": "finance"
    }
}

response = post(url, json=payload).json()
pprint(response)
```

輸出結果如下

```python
{
"copytoaster_key": "<此專案金鑰>",
"msg": 'Success!',
"status": True
}

```