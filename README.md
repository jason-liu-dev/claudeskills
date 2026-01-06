# Claude Code 安装与配置教程

## 概述

Claude Code 是一个智能编码工具，可以在终端中运行，通过自然语言命令交互帮助开发者快速完成代码生成、调试、重构等任务。

## 前提条件

在开始安装之前，请确保您的系统满足以下要求：

- **Node.js 18 或更新版本环境** - [点击下载](https://nodejs.org/en/download/)
- **Windows 用户** 还需安装 [Git for Windows](https://git-scm.com/download/win)

## 安装步骤

### 方法一：推荐安装方式

1. 打开命令行界面（终端）

2. 运行以下命令安装 Claude Code：
```bash
npm install -g @anthropic-ai/claude-code
```

3. 验证安装是否成功：
```bash
claude --version
```
如果显示版本号，则表示安装成功。

### 方法二：Cursor 引导安装方式

如果您不熟悉 Node.js 且有 Cursor 编辑器，可以在 Cursor 中输入以下命令，Cursor 会引导您完成安装：

```
https://docs.anthropic.com/zh-CN/docs/claude-code/overview Help me install Claude Code
```

## 配置 GLM Coding Plan

安装完成后，您需要配置 GLM Coding Plan 以便使用相关功能。如果您还没有智谱AI账号，可以先[注册智谱AI开放平台](https://www.bigmodel.cn/glm-coding?ic=VDMJOVV3BB)获取API密钥。

## Demo 示例：Claude Skills

为了帮助您更好地理解 Claude Code 的功能，这里有一个实际的 demo 示例项目：

### [Claude Skills Demo](https://github.com/jason-liu-dev/claudeskills)

**项目地址：** https://github.com/jason-liu-dev/claudeskills

**简介：** 这是一个演示用的 Claude Skills 仓库，包含一个示例工作流技能，展示了 Claude Code 的复杂指令跟随能力。

#### 包含的技能

**Demo Workflow (`demo-workflow`)**
- 多步骤工作流技能
- 处理输入并生成创意内容
- 将结果保存到文件中

#### 用法示例

1. 确保 Claude Code 已加载此技能
2. 在对话中输入一个主题或句子
3. 使用以下任一指令触发技能：
   - `run the demo`
   - `process this`
   - `test workflow`

**实际应用示例：**
```
用户输入：关于太空探索的未来，run the demo

Claude 将会：
1. 分析主题并提取关键词
2. 编写一个包含 "Captain Glm" 的微型科幻故事
3. 在 skills/demo-workflow/ 目录下创建一个 demo_result.md 文件保存结果
```

## 开始使用 Claude Code

1. 进入您的代码工作目录
2. 在终端中执行以下命令启动 Claude Code：
```bash
claude
```

3. 首次启动时，系统会询问「Do you want to use this API key」，选择 **Yes**

4. 选择信任 Claude Code 访问文件夹里的文件

完成以上步骤后，您就可以正常使用 Claude Code 进行开发了！

## 常见问题排查

### 手工修改配置不生效

如果您手动修改了配置文件但没有生效，请尝试以下方法：

1. **重新启动**：关闭所有 Claude Code 窗口，重新打开新的命令行窗口，再次运行 `claude` 启动

2. **重置配置**：删除 `~/.claude/settings.json` 文件，然后重新配置环境变量，Claude Code 会自动生成新的配置文件

3. **检查格式**：确认配置文件的 JSON 格式是否正确，检查变量名称和逗号使用，可以使用在线 JSON 校验工具进行检查
