# 搜尋 CopyToaster 模型

> 適用於 CopyToaster 模型

建好模型後，搜尋 CopyToaster 的模型。

```python
from requests import post
from pprint import pprint

url  = "https://api.droidtown.co/CopyToaster/Call/"

payload = {
    "project": project,
    "category": category,
    "input_str": inputSTR,
    "count": count
}

response = post(url, json=payload).json()
pprint(response)

```

輸出結果如下：

```python
{
"msg": "Success!", 
"result_list": [
    {
        "category": "...",
        "document": "...",
        "highlight": [],
        "title": "..."
    },
    {
        ...
    }
    .
    .
    .
]
}
```
