# robot-arm

机械臂比赛项目资料归档仓库。该仓库用于托管 `robot arm.zip` 及其资源说明，便于团队成员统一下载、校验和复现。

## 1. 仓库内容

当前仓库主要包含以下文件：

| 路径 | 类型 | 大小（约） | 说明 |
|---|---|---:|---|
| `robot arm.zip` | 主归档包（Git LFS） | 116.09 MiB | 完整项目压缩包（含代码、硬件资料、获奖证明、机械结构图） |

## 2. `robot arm.zip` 内部结构

压缩包顶层目录为 `robot arm/`，包含如下模块：

| 子目录 | 关键文件 | 大小（约） | 说明 |
|---|---|---:|---|
| `code/` | `first_try.zip` | 73.82 MiB | STM32 工程代码包（含 `Core/`、`Drivers/`、`Middlewares/`、`modules/`、`task/` 等目录） |
| `hardware/` | `42步进电机驱动板.zip` | 45.30 MiB | 步进电机驱动板资料（含 XDrive 开源资料、控制板代码、工程文件） |
| `honor/` | `CRAIC2025-NF-JZB7NW.pdf` | 1.45 MiB | 比赛相关荣誉/证明材料 |
| `mechanical/` | `d47e90c3-e358-4885-89c8-0b3e28f95cb1.png` | 0.19 MiB | 机械结构相关图片 |

## 3. 下载与使用

由于主压缩包超过 GitHub 单文件 100 MB 限制，本仓库使用 **Git LFS** 管理二进制文件。

### 3.1 克隆仓库

```bash
git clone https://github.com/xiaoshuaijie/robot-arm.git
cd robot-arm
git lfs pull
```

### 3.2 解压项目资料

推荐在 Windows 环境下解压（路径包含中文）：

```powershell
Expand-Archive -Path '.\robot arm.zip' -DestinationPath '.\robot arm' -Force
```

### 3.3 校验文件完整性

`robot arm.zip` 的 SHA-256：

```text
E00B4AE541BC5CF64F68D2A7FF78776F09F677ED2A477A93C58EC3E4E47F9623
```

可用如下命令复核：

```powershell
Get-FileHash -Path '.\robot arm.zip' -Algorithm SHA256
```

## 4. 工程环境建议

根据当前资料内容，建议准备以下环境：

- STM32 开发工具链（STM32CubeIDE / Keil MDK，按子工程需要选择）
- ARM GCC（如需命令行编译）
- Git + Git LFS（用于拉取主压缩包）
- 常见压缩工具（7-Zip/WinRAR/系统自带解压）

## 5. 说明与约定

- 本仓库以归档与复现为目标，尽量保持资料原始状态。
- 二进制大文件统一走 Git LFS，避免仓库历史膨胀。
- 如需新增版本资料，建议采用日期或版本号命名（例如 `robot arm_2026-03-06.zip`），并在 README 中同步更新校验信息。

## 6. 许可证与版权

本仓库仅用于比赛项目资料管理与团队协作。若包含第三方开源内容（如 XDrive 开源资料），请遵循其原始许可证条款。

