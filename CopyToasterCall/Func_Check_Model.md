# 取得 CopyToaster 部署狀態
> 適用於 `CopyToaster` 模型

檢查 CopyToaster 的模型部署狀態。

```python
from requests import post
from pprint import pprint

url  = "https://api.droidtown.co/CopyToaster/Call/"

payload = {"username": username, # 這裡填入您在 https://api.droidtown.co 使用的帳號 email。
	   "copytoaster_key": key, # 這裡填入您在 https://api.droidtown.co 登入後取得的 copytoaster_key。    
	   "func": "check_model",
	   "data": {}
}
response = post(url, json=payload).json()
return response
```
輸出結果如下：

模型部署中

```python
{
    "msg": "Model is deploying...",
    "progress_status": "processing",
    "status": true
}
```

部署完成

```python
{
"msg": "Success!", 
"progress_status": "completed", 
"status": True
}
```
