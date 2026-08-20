# HyperOS4 SmallWindow Input Filter

Restore the old HyperOS two-finger small-window gesture on HyperOS 4 (Xiaomi 17 Pro Max, Android 17).

## What it does

On older HyperOS/MIUI versions, while an app is foreground you could:

1. Swipe up from the bottom edge with your thumb and keep holding (enters recents drag).
2. Press anywhere with your index finger (nothing visible happens yet).
3. Release your thumb — the window is dragged to the index-finger position.
4. Release your index finger — the window drops into small-window mode there.

On HyperOS 4 the second finger cancels the drag instead. This LSPosed module restores the old behavior by installing an `android.view.InputFilter` inside `system_server`.

## Requirements

- Android 16+ (targetSdk 36+)
- LSPosed (libxposed API 102+)
- Root (Magisk / APatch / KernelSU)

## Install

1. Install the APK from the latest Release.
2. Enable the module in LSPosed, scope: `system` (and `com.android.systemui`).
3. Reboot.

## Notes

- Only injects into `system_server` and `com.android.systemui`.
- Debug log: `adb logcat -s SmallWindowInputFilter:I`
- Source: https://github.com/zilewang7/HyperOS4SmallWindowInputFilter

## 简介

恢复 HyperOS 4（小米 17 Pro Max，Android 17）上的旧版双指挂小窗手势。

旧版系统上：拇指从底部上滑进入多任务并按住 → 食指按住任意位置 → 松开拇指，窗口被拖到食指位置 → 松开食指，挂成小窗。HyperOS 4 上第二指会取消拖拽，本模块通过在 `system_server` 中安装 `InputFilter` 恢复旧行为。

- 需要：Android 16+、LSPosed（libxposed API 102+）、Root
- 安装：安装最新 Release 的 APK → LSPosed 中启用并勾选 `system` 作用域 → 重启
- 日志：`adb logcat -s SmallWindowInputFilter:I`
- 源码：https://github.com/zilewang7/HyperOS4SmallWindowInputFilter

## License

[MIT](LICENSE)
