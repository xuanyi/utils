
## JS截取字符串超出显示省略号

```
function cutString(str,length){
	var _str = str, _len = length;
	if(_str.length * 2 <= _len) return _str;
	var strLen = 0, newStr = '', i = 0;
	for(i < _str.length; i++){
		newStr += _str.charAt(i);
		if(_str.charCodeAt(i) > 128){
			strLen += 2;
			if(strLen >= _len){
				return newStr.substring(0,newStr.length - 1) + "...";
			}
		}else{
			strLen += 1;
			if(strLen >= _len){
				return newStr.substring(0,newStr.length - 2) + "...";
			}
		}
	}
	return newStr;
}
```
