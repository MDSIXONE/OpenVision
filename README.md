# OpenVision AI

免费、开源、非营利的单片机 IDE 项目，计划逐步替代 Keil µVision，并提供适合 AI Agent 调用的 CLI 和未来 MCP 接口。

## 当前状态

**仅完成项目目录与 GitHub 仓库初始化，尚未开始软件开发。**

目前没有可运行的 CLI、桌面应用、示例固件或构建流程。下述技术栈和功能均为规划，不代表已经实现。

## 第一阶段范围

- Windows 10/11 x64，AT89C51，默认时钟 12 MHz。
- 原生工程管理、C 代码编辑、SDCC 编译和 Intel HEX 校验与导出。
- GUI 与独立 CLI 共用 Rust 核心；初步导入 Keil XML 工程。
- 使用外部 Proteus 验证固件，本阶段不实现仿真器或硬件烧录。

计划技术栈：Rust Stable / Cargo Workspace、Tauri 2、React、TypeScript、Vite、Monaco Editor、SDCC。

## 目录

| 路径 | 规划用途 |
| --- | --- |
| `apps/cli/` | 独立 `ov` 命令行入口 |
| `apps/desktop/` | Tauri + React 桌面应用 |
| `crates/ov-core/` | 统一用例接口、执行协调和错误模型 |
| `crates/ov-project/` | 工程创建、读取、保存和配置 |
| `crates/ov-build/` | SDCC 检测、编译、日志和产物校验 |
| `crates/ov-device/` | 芯片参数和设备数据库 |
| `crates/ov-protocol/` | GUI、CLI 与未来 MCP 的公共协议 |
| `crates/ov-keil-compat/` | Keil XML 解析和迁移诊断 |
| `examples/8051-blink/` | P1.0 LED 闪烁实验 |
| `examples/8051-led-flow/` | P1 口流水灯实验 |
| `examples/8051-timer/` | Timer0 基础实验 |
| `tests/fixtures/`、`tests/integration/` | 测试数据和集成测试 |
| `docs/architecture/` | 架构文档 |
| `docs/usage/` | 使用教程 |
| `docs/compatibility/` | Keil C51 与 SDCC 兼容说明 |
| `docs/development/` | 原始需求和开发资料 |
| `.github/workflows/` | 后续 CI 工作流 |

空目录通过 `.gitkeep` 保留。尚未创建 Cargo、前端或 Tauri 配置，也未安装开发依赖。

## 需求与后续开发

完整第一阶段需求见 [原始提示词](docs/development/phase1-requirements.md)。该文档作为需求参考保留，其中的开发执行指令不构成本次初始化任务的执行范围。

收到开始开发的指令后，再检查本机工具链并逐步实现、测试和验证第一阶段功能。当前无安装包或快速运行命令。

## 许可证

自研内容采用 [MIT License](LICENSE)。未来引入的第三方依赖须单独核查并记录其许可证。
