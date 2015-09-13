# 使用命令的输出

```bat
@echo off

for /f %%i in ('date +%%Y%%m%%d_%%H%%M%%S') do (
touch %%i.txt
)

pause
```

上面的批处理脚本的功能是创建一个空txt文件，并以当前时间命名。
