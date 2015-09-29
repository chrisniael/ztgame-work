# 转义字符

```bat
@echo off

echo hello^>test.txt

pause
```

**运行结果**

```
hello>test.txt
```

`>` 是个特殊字符，用来重定向输出流的，这里要输出 `>` ，所以要通过 `^>` 来转义。
