# JS全局变量


## function外定义

```js
var name = "Tom";

function printName() {
	console.log(name);
}
```


## 不使用var，隐式的声明了全局变量

```js

yourname = "Tony";

function name() {
	name = "Tom";
}
```

不使用var定义的变量即使在函数内部，也是全局的，只要函数内的这行被执行了。


## 使用 `window.变量名` 定义

```js
window.name='Tom';

function printName() {
	console.log(window.name);
}
```

使用这样定义的全局变量的时候可以不写上 `window.`，我们常用的 `document.getXXXX` 的 `document` 对象就是 `window` 的。
