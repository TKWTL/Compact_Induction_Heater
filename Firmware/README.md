# 固件(<项目名称>)

> <填写:主控芯片 / 框架 / 一句话职责>。

## 目录组织

```text
APP/          应用层:任务 / 状态机 / 业务逻辑(Services/ 策略模块、Pages/ 页面…)
BSP/          板级支持:板卡资源与板上芯片驱动
Peripheral/   通用外设与协议抽象(总线、串口、定时、调度接口…)
Project/      厂商库与工程文件:
  Core/         器件库与系统文件
  Startup/      启动汇编
  Ld/           链接脚本
  Scheduler/    调度器(如 coroOS)
  Debug/        调试辅助(printf / 延时兼容层)
  obj/          构建产物(仅 .gitkeep 入库)
ThirdParty/   第三方源码:保持上游目录与许可证文件原样
```

## 构建

- 工具链:**<填写>**;
- 步骤:**<填写:工程打开 / 命令行构建 / 产物位置>**。

## 约定

- 分层依赖:BSP / Peripheral 不反向依赖 APP;
- 中断优先级、任务节拍等时序硬约束记录在 `Docs/FIRMWARE_ARCHITECTURE.md`;
- 第三方代码的裁剪与许可边界登记在仓库根 `THIRD_PARTY_NOTICES.md`。
