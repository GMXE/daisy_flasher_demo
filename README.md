# GMXE Flasher Demo

GMXE 固件烧录器在线演示页（单文件 HTML，HTTPS）。

**打开：<https://gmx.github.io/daisy_flasher_demo/>**

## 使用

1. 用 **Chrome / Edge** 打开上面的网址（不支持 Safari / Firefox）。
2. 让设备进入升级模式（固件升级模式，或 STM32 系统 DFU）。
3. 点击「连接设备」，在浏览器弹窗中选择 DFU 设备。
4. 选择 `.bin` 固件（或内置 Bootloader 版本），点击「开始烧录」。
5. 烧录完成后设备通常会自动复位运行。

> Windows 首次使用若识别不到设备，请安装 WinUSB 驱动（Zadig）。
>
> 本页是单文件构建，请通过上面的 HTTPS 地址使用；把 HTML 下载到本地后
> 双击以 `file://` 打开，WebUSB 通常不可用。

## 更新

在源项目执行：

```sh
python3 tools/build_single.py
```

将生成的 `dist/index.html` 覆盖本仓库的 `index.html` 后提交即可。

源项目：`GMXE/daisy_flash`（内部仓库）。
