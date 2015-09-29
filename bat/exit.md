# 退出

```bat
@echo off

echo start
exit /b 0
echo end

pause
```

**运行结果**

```
start
```

## exit 命令详解

`exit [/b] [exitCode]`

`/b` : 指定要退出当前执行的批处理脚本而不是CMD.EXE

`exitCode` : 如果指定了 `/b`，则将 `ERRORLEVEL` 设成那个数字；否则，用那个数字设置过程退出代码。
