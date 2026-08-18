# GigaRoute AI — Linux Native Preview

[English](README.md) | [한국어](README_KO.md) | **简体中文** | [日本語](README_JA.md)

**已在 Ubuntu 22.04 x86_64 环境中验证 Linux 原生运行。**

GigaRoute Auto Simulation 正在作为跨平台仿真产品进行发布准备。目前 Public Preview 已提供 Linux 原生可执行程序和独立运行包。

## Public Preview 下载

- Linux Release: https://github.com/Mega-Sim/GigaRoute_AI_Simulation_Demo/releases/tag/public-preview-526-linux
- 推荐使用的演示图纸: [`Sample/Layout_Example.dxf`](Sample/Layout_Example.dxf)

启动 Linux Demo 后，请在 **Open Layout** 中打开 `Sample/Layout_Example.dxf`。

已验证环境：

- Ubuntu 22.04 x86_64
- GCC 11.x
- Native C++/Qt6 可执行程序
- 内含 Qt runtime 的 source-free Public Preview 包

这是 GigaRoute Auto Simulation 的原生 Linux 构建版本，不是浏览器 Demo，也不是通过模拟层运行的 Windows 可执行程序。

**Public Preview 状态**

| 平台 | 状态 |
|---|---|
| Ubuntu 22.04 x86_64 | Public Preview 已发布 |
| Windows x64 | Public package 准备中 |

## Linux 运行方法

```bash
tar -xzf GigaRoute-Auto-Simulation-Demo-Linux-x86_64.tar.gz
cd GigaRoute-Auto-Simulation-Demo
chmod +x run_gigaroute.sh
./run_gigaroute.sh
```

程序启动后，请选择 **Open Layout** → `Sample/Layout_Example.dxf`。

## 安全 / 发布说明

- Linux package 中不包含 GigaRoute C/C++ 源代码。
- Public build 会避免将 application QML 原始源码直接包含在客户可执行程序中。
- Debug symbol、object file、static/import library、private build path 等开发产物会通过 release audit 排除。
- 公共 Demo DXF 仅提供整理后的演示布局。
- 下载后可使用随附的 `.sha256` 文件校验 TGZ 完整性。

> GitHub Release 自动显示的 `Source code (zip)` / `Source code (tar.gz)` 只是此 **公开 Demo 仓库的快照**，并不是 private `Sim_Core` 源码仓库。

---

## 大规模 FAB 仿真性能测试

GigaRoute Auto Simulation 的大规模半导体 FAB 布局性能测试采用了以下条件：

- 7,354 graph nodes
- 8,655 edges
- 2,066 stations
- 500 autonomous vehicles
- 8,000 moves/hour
- 2 小时仿真时间

完整的 2 小时仿真约在 7 分钟内完成，约为实时速度的 17 倍。

测试环境为普通笔记本电脑：8 GB RAM / 集成显卡。仿真过程中持续处理 vehicle following、加减速、merge control、job assignment、station reservation 和 traffic recovery，并在整个 2 小时运行中未发生系统级 gridlock。

<img width="1280" height="579" alt="image" src="https://github.com/user-attachments/assets/4ac90bb8-f133-4be7-be75-7fb334fe5284" />

当前在 CPU 利用率、日志开销和并行化方面仍有进一步优化空间。下一阶段目标是支持 1,000 → 2,000 → 3,000 台 Vehicle，同时继续提升仿真速度、内存效率和大规模交通稳定性。

GigaRoute AI  
面向大规模自主物流系统的仿真平台。
