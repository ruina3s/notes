---
title: “AI概念记录”
date: 2026-05-05
updated: 2026-05-05
author: RUINA3S
tags: [AI, 概念记录]
category: [备忘录]
description: "AI相关概念"
status: 已完成
draft: false
---

# AI概念记录

> 我有幸见证了AI时代的开启，但可惜我的工作已决定我只会是它的用户，而不是它的开发者。但我还是想作为兴趣来学习AI相关概念，以便更好地理解和应用AI技术。
> 
> —— RUINA3S

## 概念们

### 1.LLM（Large Language Model）
LLM（大型语言模型）是通过训练大量文本数据而获得的能力，能够生成人类语言。我们可以把它看成是相关AI程序的"引擎"

### 2.tokenizer
负责在用户与LLM之间进行文本与数组的转换(编码:将文本转换为token序列，解码:将token序列转换为文本)，将用户输入的文本转换为LLM可以理解的token序列，同时将LLM的输出序列转换为用户可以理解的文本。

![编码](https://gcore.jsdelivr.net/gh/ruina3s/imgs@main/20260505195901.png)

![tokenizer运行过程](https://gcore.jsdelivr.net/gh/ruina3s/imgs@main/20260505200004.png)

token：大模型处理文本的最基本单位

[字节跳动旗下火山引擎token计算器工具](https://console.volcengine.com/ark/region:ark+cn-beijing/tokenCalculator?)

[百度文心一言 Token 计算器](https://console.bce.baidu.com/support//tokenizer)

[阿里通义千问 Token 计算器](https://dashscope.console.aliyun.com/tokenizer)

[ToolSnak AI Token 计数器](https://www.toolsnak.com/zh/ai-token-jishuqi )

### 3.context
上下文：在LLM中，用户输入的文本（或之前生成的文本）作为LLM的输入，被LLM处理后，再输出给用户。这个过程被称为上下文。

通过这种方式能够让AI工具记住之前的信息。

context window：上下文窗口，context能够处理的最大token量

RAG：Retrieval-Augmented Generation，检索增强生成，是指在生成文本时，利用检索到的上下文信息来增强生成文本的质量和相关性。即简化了生成文本的复杂，提高了生成文本的准确性和相关性。

### 4.Prompt
Prompt（提示词）是指用户输入给LLM的文本，用于引导LLM生成特定的输出。Prompt可以是一个问题、一个命令、一个描述或者任何形式的文本，旨在引导LLM生成符合用户需求的文本。

![提示词分类](https://gcore.jsdelivr.net/gh/ruina3s/imgs@main/20260505202744.png)

### 5.tool
Tool（工具）是指在LLM的基础上，结合其他功能模块或外部资源，提供特定功能的AI应用程序。Tool可以是一个独立的应用程序，也可以是一个集成在LLM中的功能模块，旨在满足用户的特定需求。

### 6.MCP（Model Call Protocol）
MCP（模型调用协议,**统一的接入规范**）是指LLM与Tool之间的通信协议，用于在LLM和Tool之间传递信息和指令。MCP定义了LLM和Tool之间的交互方式，包括请求和响应的格式、错误处理机制等。

### 7.agent（智能体）
Agent（智能体）是指在LLM和Tool的基础上，结合MCP协议，能够自主地完成特定任务的AI系统。Agent能够根据用户的需求，选择合适的Tool，并通过MCP协议与Tool进行交互，以完成用户的任务。

### 8.agent skill
Agent Skill给agent看的说明文档，用md格式书写，放在agent工具指定目录下。

### 9.harness
Harness（测试工具）是指用于测试和评估LLM、Tool和Agent性能的工具。Harness可以模拟用户的输入，测试LLM、Tool和Agent的响应，并评估其性能和准确性。(调整系统)

### 10.多模态
多模态是指在LLM、Tool和Agent中，能够同时处理多种模态数据（如文本、图像、视频等）。多模态的处理能够提高模型的性能和准确性，因为它能够利用不同模态的信息来生成更准确的输出。

### 11.AIGC（AI生成内容）
AIGC（AI生成内容）是指利用AI技术自动生成内容，如文本、图像、视频等。AIGC的出现，为内容创作提供了新的可能性，也为内容消费提供了新的体验。