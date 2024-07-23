# 建立新的分類

> 適用於 CopyToaster 模型

在 CopyToaster 專案中建立一個分類 (category)

```python
from requests import post
from pprint import pprint 

url  = "https://api.droidtown.co/CopyToaster/Call/"

payload = {"username": username, # 這裡填入您在 https://api.droidtown.co 使用的帳號 email。
           "copytoaster_key": key, # 這裡填入您在 https://api.droidtown.co 登入後取得的 copytoaster key。
           "category": "存匯",
           "func": "create_category",
           "data": {}
 }
 
 response = post(url, json=payload).json()
```

輸出結果如下

```python
{
"msg": "Success!", 
"status": True
}
```
