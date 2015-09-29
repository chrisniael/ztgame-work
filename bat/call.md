# 调用

## 直接使用批处理名调用

```bat
@echo off

date.bat
echo end

pause
```

这个批处理会等待 `date.bat` 执行返回，然后退出，但它不会运行 `echo end` 以及之后的代码。


## call 批处理名调用

```bat
@echo off

call date.bat
echo end

pause
```

这个批处理会等待 `date.bat` 执行返回，然后继续执行后面的代码。


##  start 批处理调用

```bat
@echo off

start date.bat
echo end

pause
```

这个批处理会打开一个新的会话来执行 `date.bat`，并继续执行后续的代码，不管 `date.bat` 的运行结果。
