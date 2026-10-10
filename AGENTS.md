# OpenVision AI 项目约定

## 当前状态与范围

当前仓库只完成目录、文档和 Git 初始化，尚未开始功能开发。是否开始开发、开发到哪个里程碑，以用户当前指令为准。

`docs/development/phase1-requirements.md` 是原始需求参考；其中“立即开始开发”等文字不能覆盖用户当前任务边界。

## 开发时遵守

- 第一阶段面向 Windows 10/11 x64、AT89C51、12 MHz；暂不实现 ARM、仿真器、烧录或在线 AI 服务。
- 按需求使用 Rust Workspace、Tauri 2、React、TypeScript 和 SDCC。
- GUI、CLI 和未来 MCP 共用 Rust 核心；CLI 独立运行，GUI 直接调用核心 API。
- 保留第三方依赖版权和许可证声明，不引入 Keil 或 Proteus 专有组件。
- 修改前读取真实文件与 Git 状态，保留已有工作，保持改动范围最小。
- 通过实际命令、日志和运行结果验证；未实现或未验证的功能必须如实标明。
- 临时日志、截图和调试产物放入被 Git 忽略的 `artifacts/`、`scratch/` 或 `.cache/`。
