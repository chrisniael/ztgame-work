# 流重定向

## 标准输出流重定向

```bat
@echo off

@echo hello
@echo hello >nul
@echo hello 1>nul

pause
```


## 标准错误输出流重定向

```bat
@echo off

errorcmd 2>nul
errorcmd 1>nul 2>&1

pause
```
