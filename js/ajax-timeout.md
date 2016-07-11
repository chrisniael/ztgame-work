# AJAX 设置超时时间

```js
var ajaxTimeOutTest = $.ajax({
    url: "example.com/index.php",
    timeout: 1000,      //设置超时时间
    type: "get",
    data: {},
    dataType: "json",
    success: function(data) {
    },
    complete: function(XMLHttpRequest, status) {
        if(status == "timeout") {       //status 还包含 success, error 等值
            ajaxTimeOutTest.abort();
            alert("超时");
        }
    }
```
