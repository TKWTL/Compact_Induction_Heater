# <项目名称>

> 一句话:**<填写:主控芯片 / 核心功能 / 形态>**。

本仓库由 `Project_Template` 初始化:目录组织、`.gitignore` / `.gitattributes`、
许可与第三方声明均已就位。使用方式:复制本文件夹为新工程目录并重命名,替换全部
`<填写>` 占位,确认 `LICENSE`(默认 AGPL-3.0,可换)与第三方声明后开始开发。

## 1. 目录结构

| 路径 | 内容 |
|---|---|
| `Docs/` | 文档:固件架构、移植笔记、装配指南、测试报告、用户手册 |
| `Firmware/` | 固件工程(分层见 [`Firmware/README.md`](Firmware/README.md)) |
| `Hardware/` | 硬件:`source/` 设计源、`Preview/` 预览/网表、`Manufacturing/` 生产文件 |
| `Images/` | 图片素材:`Product/` `Assembly/` `Testing/`(见 [`Images/README.md`](Images/README.md)) |
| `LICENSE` | 开源协议(默认 **GNU AGPL-3.0-only**) |
| `THIRD_PARTY_NOTICES.md` | 第三方组件来源 / 许可证 / 使用边界声明 |

```text
<项目>/
├── Docs/                      固件架构 / 移植 / 装配 / 测试 / 用户手册
├── Firmware/
│   ├── APP/                   应用层:任务、状态机、业务/页面(Services/ 策略模块…)
│   ├── BSP/                   板级支持:板卡资源与板上芯片驱动
│   ├── Peripheral/            通用外设与协议抽象(总线、串口、定时…)
│   ├── Project/               厂商库与工程文件
│   │   ├── Core/              器件库与系统文件
│   │   ├── Startup/           启动汇编
│   │   ├── Ld/                链接脚本
│   │   ├── Scheduler/         调度器(如 coroOS)
│   │   ├── Debug/             调试辅助(printf / 延时兼容层)
│   │   └── obj/               构建产物(仅 .gitkeep 入库)
│   └── ThirdParty/            第三方源码(保留上游目录与许可证文件)
├── Hardware/
│   ├── Manufacturing/         生产文件(Gerber/BOM/坐标…)
│   ├── Preview/               预览、网表、原理图导出
│   └── source/                EDA 工程源
└── Images/                    Assembly / Product / Testing
```

## 2. 快速开始

- 工具链:**<填写:IDE / 编译器版本>**;
- 构建:**<填写:构建步骤>**;
- 烧录:**<填写:烧录方式与注意事项>**。

## 3. 版本记录

| 版本 | 日期 | 内容 |
|---|---|---|
| v0.1 | <填写> | 初始版本 |

## 4. 许可(协议声明)

- **项目自写代码默认采用 GNU AGPL-3.0-only**(见 [`LICENSE`](LICENSE));
  如需更换协议:替换 `LICENSE` 全文,并同步修改本节与各源码文件头(如有);
- **第三方组件**:任何随仓库分发的外部源码(厂商库、图形库、调度器等)必须保留
  上游版权与许可通知,并登记到 [`THIRD_PARTY_NOTICES.md`](THIRD_PARTY_NOTICES.md);
  仓库级 AGPL 声明**不会**替换或减免上游声明的效力;
- **硬件工程文件**(CAD / Gerber / 结构件)的发布范围与许可:**<填写:随仓库发布 / 另行约定>**。

## 5. 资料与参考

- 芯片数据手册:**<填写>**;
- 参考项目:**<填写>**。

## 6. AI 辅助声明

- **适用范围**:AI 辅助**仅用于**<填写:如固件代码与文档;硬件为全人工设计>;
- **使用工具**:<填写:如 DeepSeek / GPT / GitHub Copilot 等>;
- **具体用途**:代码与注释的初稿、重构建议;文档的撰写与润色;资料理解与排查思路
  整理。编译、上板与实测均由人工完成;
- **责任声明**:所有 AI 生成内容均经人工审查、修改并在实物上验证;设计决策与测试
  结论由项目作者负责。AI 输出不提供任何正确性担保,复刻或二次开发时请自行核对与
  验证。
