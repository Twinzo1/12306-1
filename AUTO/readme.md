# win10 子系统环境，其它环境未测试
* 浏览器油猴脚本安装 [地址](https://github.com/Famine-Life/get12306cookie)
* 修改脚本
```
// 修改发送的url
var text = JSON.stringify(data)
var obj = JSON.parse(text);
xmlhttp.open("GET", "http://127.0.0.1:5000/set_tk/" + obj.tk, true);
xmlhttp.open("GET", "http://127.0.0.1:5000/set_rd/" + obj.RAIL_DEVICEID, true);
xmlhttp.open("GET", "http://127.0.0.1:5000/set_re/" + obj.RAIL_EXPIRATION, true);
xmlhttp.setRequestHeader('Content-Type','application/x-www-form-urlencoded');
console.log("JSON==================",obj.tk);
```
## TODO
* 使用FastAPI实现（与当前方式相差不大）
