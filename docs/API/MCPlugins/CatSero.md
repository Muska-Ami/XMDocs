## 查询版本

### 方法概要

`HTTP GET`

地址：`https://api.huahuo-cn.tk/mcplugins/CatSero/version`

### 请求参数

无

### 返回数据

```json
{
	"latest": {
		"tag": "(Tag)",
		"html_url": "(Latest release HTML url)"
	},
	"beta": {
		"jar_zip": "(Beta JAR api url)",
		"full_zip": "(Beta Artifact api url)"
	},
	"other": {
		"latest_limit": (Latest limit),
		"beta_limit": (Beta limit)
	}
}
```
