# SourceTree for windows 安装

## 免注册操作

### 1. 打开计算机或此电脑<img src="amWiki/images/图片 28.png" style="zoom:50%" />
<img src="amWiki/images/图片 24.png" style="zoom:80%" />

### 2. 在地址栏输入  %LocalAppData%\Atlassian\SourceTree\   回车

### 3. 在下图2的区域新建一个 accounts.json 文件，然后把下列代码拷贝到里面保存。

```json
[
  {
  "$id": "1",
  "$type": "SourceTree.Api.Host.Identity.Model.IdentityAccount, SourceTree.Api.Host.Identity",
  "Authenticate": true,
  "HostInstance": {
   "$id": "2",
   "$type": "SourceTree.Host.Atlassianaccount.AtlassianAccountInstance, SourceTree.Host.AtlassianAccount",
   "Host": {
     "$id": "3",
     "$type": "SourceTree.Host.Atlassianaccount.AtlassianAccountHost, SourceTree.Host.AtlassianAccount",
     "Id": "atlassian account"
   },
   "BaseUrl": "https://id.atlassian.com/"
  },
  "Credentials": {
   "$id": "4",
   "$type": "SourceTree.Model.BasicAuthCredentials, SourceTree.Api.Account",
   "Username": "",
   "Email": null
  },
  "IsDefault": false
  }
]
```

<img src="amWiki/images/图片 29.png" style="zoom:50%" />
