# 建立 CopyToaster 文件

> 適用於 CopyToaster 模型

在 CopyToaster 中的 "存匯" 分類 (category) 中建立文件 (document)

```python
from requests import post
from pprint import pprint

url  = "https://api.droidtown.co/CopyToaster/Call/"

payload = {
	"username": username, # 這裡填入您在 https://api.droidtown.co 使用的帳號 email。
	"copytoaster_key": key, # 這裡填入您在 https://api.droidtown.co 登入後取得的 copytoaster_key。
	"category": "存匯",
	"func": "insert_document",
	"data": {
	"document": [{"title": "範例標題",
		      "content": "範例內容",
    		      "hashtag": ["範例內容"
     		                 ]
	              }]
	}
}

response = post(url, json=payload).json()
pprint(response)
```

輸出結果如下

```python
{
"msg": "Success!",
"result_list": [
 	{"msg": "Success!", "status": True}
],
"status": True
}
```

