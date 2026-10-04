# PVZ 杂交版 · 鸿蒙移植版

《植物大战僵尸杂交版重制版》的 HarmonyOS NEXT / OpenHarmony 移植版。

> **非官方项目**，与任何原作权利方无关联，仅供爱好者交流测试。

## 下载

最新安装包见 [Releases](../../releases) 页面。

## 运行环境

| 项 | 要求 |
| --- | --- |
| 系统 | HarmonyOS NEXT / OpenHarmony 6.x |
| 架构 | **arm64-v8a** |
| 引擎 | Godot 4.4.1.stable.mono + NativeAOT (linux-musl-arm64) |

## 安装

1. 设备开启「开发者模式」+「USB 调试」
2. 连接电脑后执行：

   ```bash
   hdc install -r PVZ-Hybrid-0.29-harmonyos-arm64-unsigned.hap
   ```

> 本包**未签名**，需自行签名，或使用已授权的开发者设备。

## 技术说明

移植工作集中在**引擎与资源格式层面**，未改动游戏玩法逻辑：

- Godot 4.7 -> 4.4.1 降级重编译（C# 源码 NativeAOT 交叉编译至 musl-arm64）
- PCK 资源包 v4 -> v2 格式降级重导出
- ICU / OpenSSL 依赖替换为设备可用实现，并随包内置 CA 根证书

## 免责声明

非官方项目，仅供技术交流与学习，请勿用于商业用途。
