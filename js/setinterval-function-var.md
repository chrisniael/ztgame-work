# setInterval、setTimeOut传递带参数的函数


## 采用字符串形式

```js
function loading(content) {
	console.log(content);
}

setInterval("loading(content)", 1000);
```


## 匿名函数包装

```js
function loading(content) {
	console.log(content);
}

setInterval(function() {
	loading(content);
	}, 1000);
```


## 定义返回无参函数的函数

```js
function loading(content) {
	console.log(content);
}

function _loading(content) {
	return function()
	{
		loading(content);
	}
}

window.setInterval(_foo(id),1000);
```
