# CentOS Text 模式分辨率设置

CentOS 以 Minimal 方式安装的话，Text 模式下，默认的分辨率为 `640 x 480`，下面将分辨率设置为 `1920 x 1280`

* 编辑文件 `/etc/default/grub`，修改 `GRUB_CMDLINE_LINUX` 字段，在其值末尾添加 `vga=0x354`
    
    ```shell
    GRUB_CMDLINE_LINUX="crashkernel=auto rd.lvm.lv=centos/root rd.lvm.lv=centos/swap rhgb quiet vga=0x354"
    ```

    `vga` 的值 `0x354` 对应分辨率 `1920 x 1080`，想要设置为其他分辨率只需要将 `vga` 设置为相应值即可。


* 使用 `grub2-mkconfig` 来重新生成 `/boot/grub2/grub.cfg` 文件

    ```shell
    grub2-mkconfig -o /boot/grub2/grub.cfg
    ```

* `reboot` 重启后生效。

## vga 值 与 分辨率对应表（部分）

| vga (十六进制) | 分辨率       |
| -------------- | ------------ |
| 0x31C          | 640x480x32   |
| 0x356          | 1360x768x32  |
| 0x33F          | 1440x900x32  |
| 0x353          | 2560x1600x32 |
| 0x354          | 1920x1080x32 |

这里省略了很多，要查看完整的分辨率表，可以使用一个错误的 `vga` 值，然后按照上面的步骤重启后，CentOS 会检测到你使用的 `vga` 值是无效的，按 `Enter` 键后，会列出所有支持的分辨率以及对应的 `vga` 值。
