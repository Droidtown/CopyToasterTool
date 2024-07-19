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
	"document": [
	{
	 	"title": "我要如何註銷行動無卡提款服務呢？",
	 	"content": "方法一、請您登入行動銀行→點選「設定」→點選「無卡提款服務設定」→點選「我要註銷」，閱讀註銷說明後，按下「確認」即可完成註銷。\n方法二、您也可以前往玉山銀行ATM→點選螢幕「無卡提款」→「註銷」→輸入「身分證字號」→輸入「無卡交易密碼」，確認您要註銷行動無卡提款服務即可註銷成功。",
	 	"hashtag": [
	 		"存匯",
	 		"無卡提款"
     	]
	}
	]
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
 	{"msg": "Success!", "status": True},
 	{"msg": "Success!", "status": True}
],
"status": True
}
```

