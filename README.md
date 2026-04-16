# Deskgram 2 代理管理

代理管理是 Deskgram 2 的基础设施模块，用于存储、导入、检测并分配 Telegram 账号使用的代理。它适合为私信、邀请、收集和其他自动化场景准备稳定的运行环境。

[Deskgram 2 中文总览](https://github.com/Deskgram-2/deskgram-2-telegram-automation-zh) | [官网](https://deskgram2.com/) | [Telegram Bot](https://t.me/DG2welcomebot) | [Web Preview](https://deskgram2.com/web-preview)
## 交互式 Web Preview

[![Interactive Demo](https://img.shields.io/badge/DEMO-Try_in_Browser-brightgreen?style=for-the-badge&logo=google-chrome)](https://deskgram2.com/web-preview?path=%2Fapp-demo%2Ffunctions%2Fproxy)

在浏览器中体验这个模块: [打开 Web Preview](https://deskgram2.com/web-preview?path=%2Fapp-demo%2Ffunctions%2Fproxy)



## 模块简介

| 参数 | 内容 |
|---|---|
| 核心任务 | 存储、导入和检测 Telegram 代理 |
| 支持类型 | `SOCKS5`, `HTTP` |
| 适用场景 | 账号网格、私信活动、邀请、收集 |
| 核心动作 | 批量导入、检测、筛选、账号绑定 |
| 关联模块 | 账号面板、邀请模块、设置 |

## 模块能力

- 展示统一的代理表格；
- 从准备好的列表中批量导入代理；
- 检查可用性和响应状态；
- 把代理绑定到 Telegram 账号；
- 为自动化模块维护可复用的代理池；
- 把基础设施集中在一个位置管理。

## 快速开始

1. 导入代理列表。
2. 执行基础检测并剔除无效项。
3. 把可用代理绑定到目标账号。
4. 在邀请、私信或收集流程中复用准备好的代理池。

## 这套代理基础通常会接到哪些执行模块

- [私信群发](https://github.com/Deskgram-2/telegram-direct-messaging-deskgram-zh)，当触达流程需要稳定的账号环境；
- [邀请模块](https://github.com/Deskgram-2/telegram-invite-tool-deskgram-zh)，当账号和受众基础已经准备好并要继续执行增长；
- [受众收集](https://github.com/Deskgram-2/telegram-audience-parser-deskgram-zh)，当代理支撑的数据收集在前面；
- [加群模块](https://github.com/Deskgram-2/telegram-join-groups-deskgram-zh)，当社区参与场景依赖健康的基础设施；
- [账号面板](https://github.com/Deskgram-2/telegram-account-manager-deskgram-zh)，当你想先把可用代理绑定到具体账号网格上。

## 适合在什么情况下使用

- 当很多 Telegram 账号同时工作；
- 当你希望把代理管理集中在一个可见位置；
- 当邀请、收集和触达都依赖稳定基础设施；
- 当账号绑定不能继续依赖零散维护。

## 相比手动管理代理更方便的地方

| 手动方式 | Deskgram 2 代理管理 |
|---|---|
| 代理数据分散在多个文件里 | 提供统一代理表格 |
| 检测耗时且不稳定 | 健康检测是工作流一部分 |
| 账号绑定容易混乱 | 绑定过程可见且可复用 |
| 难以长期维护同一代理池 | 代理基础集中管理 |
| 基础设施维护成本高 | 更适合持续清理和更新 |

## 适用场景

- 为 [私信群发](https://github.com/Deskgram-2/telegram-direct-messaging-deskgram-zh) 准备稳定代理池，适合多账号触达场景；
- 在 [邀请模块](https://github.com/Deskgram-2/telegram-invite-tool-deskgram-zh) 和 [加群模块](https://github.com/Deskgram-2/telegram-join-groups-deskgram-zh) 之前先把基础设施准备好；
- 支撑 [受众收集](https://github.com/Deskgram-2/telegram-audience-parser-deskgram-zh)，当流程从 discovery 和数据采集开始时；
- 统一轮换和清理可重复使用的代理层，让多个 Deskgram 2 工作流共用一套稳定环境。

## 先做什么更合适：代理管理还是账号面板

| 如果你的目标是 | 更适合先做什么 |
|---|---|
| 先把账号网格整理清楚 | [账号面板](https://github.com/Deskgram-2/telegram-account-manager-deskgram-zh) |
| 先检查连接质量并剔除不稳定节点 | `代理管理` |
| 为大规模执行准备稳定底座 | 先做账号面板，再进入 `代理管理` |
| 在启动前统一工作区环境 | 先处理账号和代理，再去 [设置](https://github.com/Deskgram-2/telegram-automation-settings-deskgram-zh) |

## 相关仓库

- [Deskgram 2 中文总览](https://github.com/Deskgram-2/deskgram-2-telegram-automation-zh)
- [账号面板](https://github.com/Deskgram-2/telegram-account-manager-deskgram-zh)
- [邀请模块](https://github.com/Deskgram-2/telegram-invite-tool-deskgram-zh)
- [设置](https://github.com/Deskgram-2/telegram-automation-settings-deskgram-zh)
- [私信群发](https://github.com/Deskgram-2/telegram-direct-messaging-deskgram-zh)
- [受众收集](https://github.com/Deskgram-2/telegram-audience-parser-deskgram-zh)
- [加群模块](https://github.com/Deskgram-2/telegram-join-groups-deskgram-zh)

## FAQ

### 常见代理类型有哪些？

通常围绕 `SOCKS5` 和 `HTTP` 工作。

### 为什么要单独做一个代理模块？

因为把基础设施从具体执行模块中拆出来，会更容易维护和复用。

### 哪些模块最依赖它？

邀请、收集、私信，以及所有需要大规模账号网格的工作流。
