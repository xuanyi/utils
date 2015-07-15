## 获取Url参数queryString

- 返回单个属性值

```
function queryString(url,name){
	var reg = new RegExp('(^|&)' + name + '=([^&]*)(&|$)', 'i');
	var r = url.split('?')[1].match(reg);
	if(r != null){
		return unescape(r[2]);
	}
	return null;
}
```

- 返回对象
