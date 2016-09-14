# 设置 SIP

SIP 全称是系统完整性保护（System Itegrity Protection），是用来限制 root 账号的文件操作权限的。


## 打开/关闭 SIP

* 重启 Mac，启动时按住 `Command` 和 `R` 键进入恢复模式

* `Utilities` -> `Terminal`，打开终端

* 查看 SIP 设置状态

    ```shell
    csrutil status
    ```
* 设置 SIP 打开/关闭

    ```shell
    csrutil enable
    ```
    这是打开 SIP，下面是关闭的

    ```shell
    csrutil disable
    ```
* 更改完 SIP 设置后，需要重启 Mac 来使设置生效。

## 参考资料

* [How to Disable System Integrity Protection on a Mac (How-To Geek)](http://www.howtogeek.com/230424/how-to-disable-system-integrity-protection-on-a-mac-and-why-you-shouldnt/)
* [Configuring System Integrity Protection (Developer Apple)](https://developer.apple.com/library/content/documentation/Security/Conceptual/System_Integrity_Protection_Guide/ConfiguringSystemIntegrityProtection/ConfiguringSystemIntegrityProtection.html)
