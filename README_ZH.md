# GigaRoute AI — Linux Native Preview

[English](README.md) | [한국어](README_KO.md) | **简体中文** | [日本語](README_JA.md)

**已在 Ubuntu 22.04 x86_64 环境中验证 Linux 原生运行。**

GigaRoute Auto Simulation 正在作为跨平台仿真产品进行发布准备。目前 Public Preview 已提供 Linux 原生独立运行包。

## Quick Start — 应该下载哪些文件？

### 1. 从 GitHub Release 下载程序

**Linux Release:** https://github.com/Mega-Sim/GigaRoute_AI_Simulation_Demo/releases/tag/public-preview-526-linux

请在 Release 页面下方的 **Assets** 中下载：

`GigaRoute-Auto-Simulation-Demo-Linux-x86_64.tar.gz`

> **`Source code (zip)` / `Source code (tar.gz)` 不是 GigaRoute 应用程序。** 它们是 GitHub 自动生成的公开 Demo 仓库快照，无需作为程序下载。

可使用随附的 `.sha256` 文件验证应用程序包完整性。

### 2. 从 Repository 单独下载示例 DXF

**示例图纸:** [`Sample/Layout_Example.dxf`](Sample/Layout_Example.dxf)

示例图纸与 Release 程序包分开维护在 Repository 的 `Sample/` 文件夹中。打开上方文件链接后，使用 **Download raw file** 将 `Layout_Example.dxf` 保存到本地。

### 3. 运行程序

```bash
tar -xzf GigaRoute-Auto-Simulation-Demo-Linux-x86_64.tar.gz
cd GigaRoute-Auto-Simulation-Demo
chmod +x run_gigaroute.sh
./run_gigaroute.sh
```

启动后：

**Open Layout → 选择单独下载的 `Layout_Example.dxf` → 运行 Simulation。**

## 视图操作与快捷键

GigaRoute 的 2D 和 3D 视图使用不同的导航方式。开始使用时不需要记住全部快捷键；通常只需要掌握鼠标滚轮、平移和旋转即可。

### 2D 视图

| 输入 | 功能 |
|---|---|
| **鼠标滚轮** | 以鼠标位置为中心放大 / 缩小 |
| **鼠标中键（MMB）+ 拖动** | 平移图纸 |
| **Shift + 鼠标左键（LMB）+ 拖动** | 平移图纸 |
| **Ctrl + Shift + LMB + 拖动** | 拖动缩放 |
| **LMB** | 选择对象 |
| **双击 LMB 后拖动** | 平移视图 |
| **V**、**Home** 或 **0** | 将完整图纸自动适配到当前窗口 |
| **Ctrl + T** | 显示 / 隐藏图纸与 Station 文本 |
| **Ctrl + D** | 显示 / 隐藏方向箭头 |

**推荐的 2D 操作：** 使用 **鼠标滚轮**缩放，使用 **MMB + 拖动**或 **Shift + LMB + 拖动**移动大型图纸。如果缩放或平移后找不到图纸，可按 **V / Home / 0** 恢复完整视图。

### 3D 视图

| 输入 | 功能 |
|---|---|
| **鼠标滚轮** | 放大 / 缩小 |
| **Ctrl + LMB + 拖动** | 旋转相机（Orbit） |
| **MMB + 拖动** | 平移相机 |
| **Shift + Alt + LMB + 拖动** | 备用平移操作 |
| **Ctrl + Shift + Alt + LMB + 拖动** | 相机前后移动（Dolly） |
| **LMB + 拖动** | 框选对象 |
| **鼠标右键（RMB）** | 打开 Context Menu |
| **Ctrl + D** | 显示 / 隐藏 3D 方向标记 |

**推荐的 3D 操作：** 使用 **Ctrl + LMB + 拖动**旋转模型，使用 **MMB + 拖动**平移，并使用**鼠标滚轮**缩放。

### 鼠标按键缩写

- **LMB** = 鼠标左键
- **MMB** = 鼠标中键 / 滚轮按下
- **RMB** = 鼠标右键

> 提示：如果在 2D 视图中找不到图纸，请按 **V**、**Home** 或 **0** 将完整布局重新适配到屏幕。

### 下载位置摘要

- **应用程序:** 仅从 GitHub **Releases / Assets** 下载
- **示例 DXF:** 从 Repository **`Sample/` 文件夹**下载
- **GitHub Source code 压缩包:** 不是应用程序下载文件

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
