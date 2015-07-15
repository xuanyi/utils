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

```
function queryString(url){
	var params = {};
	var _url = url !== undefined ? url : window.location.search;
	if(typeof _url === 'string' && _url.length > 0){
		if(_url[0] === '?'){
			_url = _url.substring(1);
		}
		var paramArr = _url.split('&'), i = 0;
		for(i < paramArr.length; i++){
			var item = paramArr[i];
			var pos = item.indexOf('=');
			var key = item.substr(0,pos);
			var value = item.substr(pos + 1);
			if(pos >= 0){
				params[key] = value;
			}else{
				params[key] = '';
			}
		}
	}
	return params;
}
```
