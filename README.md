# HyperOS4 SmallWindow Input Filter

Restore the old HyperOS two-finger small-window gesture on HyperOS 4 (Xiaomi 17 Pro Max, Android 17).

## What it does

On older HyperOS/MIUI versions, while an app is foreground you could:

1. Swipe up from the bottom edge with your thumb and keep holding (enters recents drag).
2. Press anywhere with your index finger (nothing visible happens yet).
3. Release your thumb — the window is dragged to the index-finger position.
4. Release your index finger — the window drops into small-window mode there.

On HyperOS 4 the second finger cancels the drag instead. This module uses the unified MiuiHome HYOS native runtime path provided by Zygisk Next and LSPosed IT to retain the original launcher gesture route.

## Requirements

- Official HyperOS 4 / Android 17 firmware, arm64-v8a
- Zygisk Next 1.5.0+
- LSPosed IT 2.1.1+ with HYOS-spawner support (libxposed API 102)
- Validated MiuiHome profile: `801025361` / `RELEASE-8.01.02.5361-260807-08161657-R`
- Root (Magisk / APatch / KernelSU)

Modified official ROMs and ported/custom ROMs are not supported. Report their runtime or gesture differences to the ROM maintainer.

## Install

1. Install the APK from the latest Release.
2. Enable the module in LSPosed, scope: `com.miui.home`.
3. Reboot.

## Notes

- Native log: `adb logcat -s SmallWindowNative:I`
- Diagnostics build: every release also carries `io.github.zilewang7.smallwindow-*_debug_diag.apk`; it writes to `/data/user_de/0/com.miui.home/cache/smallwindow_native.log` (root-readable)
- Source: https://github.com/zilewang7/HyperOS4SmallWindowInputFilter

## 简介

恢复 HyperOS 4（小米 17 Pro Max，Android 17）上的旧版双指挂小窗手势。

旧版系统上：拇指从底部上滑进入多任务并按住 → 食指按住任意位置 → 松开拇指，窗口被拖到食指位置 → 松开食指，挂成小窗。HyperOS 4 上第二指会取消拖拽，本模块通过 Zygisk Next 与 LSPosed IT 提供的统一 MiuiHome HYOS native runtime 路径恢复桌面原生处理。

- 需要：官方 HyperOS 4 / Android 17、arm64-v8a、Zygisk Next 1.5.0+、LSPosed IT 2.1.1+（支持 HYOS spawner / libxposed API 102）、Root
- 已验证桌面：`801025361` / `RELEASE-8.01.02.5361-260807-08161657-R`
- 不支持官改包、移植包及其他第三方修改系统；请向对应系统维护者反馈
- 安装：安装最新 Release 的 APK → LSPosed 中启用并勾选 `com.miui.home` 作用域 → 重启
- 日志：`adb logcat -s SmallWindowNative:I`
- 诊断版：每个 Release 附带 `io.github.zilewang7.smallwindow-*_debug_diag.apk`，日志写入 `/data/user_de/0/com.miui.home/cache/smallwindow_native.log`（root 可读）
- 源码：https://github.com/zilewang7/HyperOS4SmallWindowInputFilter

## License

[MIT](LICENSE)
