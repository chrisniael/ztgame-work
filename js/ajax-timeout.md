# AJAX 设置超时时间

```js
var ajaxTimeOutTest = $.ajax({
    url: "example.com/index.php",
    timeout: 1000,      //设置超时时间
    type: "POST",
    async: true,
    data: {},
    dataType: "json",
    success: function(data, textStatus) {
    },
    complete: function(XMLHttpRequest, status) {
        if(status == "timeout") {       //status 还包含 success, error 等值
            ajaxTimeOutTest.abort();
            alert("超时");
        }
    }
```

`timeout` 字段指定了 `ajax` 的超时时间。如果 `ajax` 执行超过了这个时间，则会调用 `complete` 字段指定的函数，并且传递过来的 `status` 的字段为 `timeout`。
