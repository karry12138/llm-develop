20231113-1114 by 老年人elderman
Task01 大模型简介
### 概述
Large Language Model,指的是参数达到百亿及以上的语言模型。其与参数在亿及以下量级的类似架构小语言模型相比，最大的特点是”涌现”出了解决复杂问题的能力，诸如上下文学习，遵循并完成用户自然语言指令输入，以及逐步的逻辑推理。国外常见的大模型为GPT-3,GPT-4,PaLM,LLaMA等，国内的有清华与智谱AI开发的GLM,百度文心一言，科大讯飞的讯飞星火等。它们的出现使得通用人工智能AGI变得可能。

### 常见大模型
#### 开源
Baichuan - 百川智能 可商用 参数量7B/13B 上下文4K 中英双语 
基底模型(开发者可微调)+对话模型 https://github.com/baichuan-inc

GLM系列 - 清华大学+智谱AI 截止20231114已发布到ChatGLM3，中文社群好
有相当数量的变种大模型，很惊艳。部分变种如下

++++++++

CogVLM 多模态(语言+图片)，可以理解图片并基于此进行推理和对话。也包含OCR功能。部分情况下识别的图片细节比GPT-4-vision模型更多
模型推理: 1*A100(80g) / 2*RTX 3090 (24g)
微调:4*A100(80g) / 8*RTX 3090 (24g)
https://github.com/THUDM/CogVLM

VisualGLM-6B 使用显存小(15G,可INT4),发布时间比CogVLM早的多模态大模型
https://github.com/THUDM/VisualGLM-6B

ChatGLM3-6B 双语对话 可api调用 上下文8k-32k 所需显存默认13G(可INT4量化)。DEMO项目中提供了对话，外部工具调用和代码解释器3种模式。
https://github.com/THUDM/ChatGLM3

CodeGeeX2 代码生成大模型 支持多种编程语言 支持vscode等多种常见IDE的插件 上下文8K,量化后仅需6G显存
https://github.com/THUDM/CodeGeeX2

++++++++

LLaMA系列 使用公开数据集进行训练的代表,使用的数据集有Common Crawl、Wikipedia、OpenWebText2、RealNews、Books 。参数量7B-70B
(英文看着头疼)
https://github.com/facebookresearch/llama

通义千问 阿里巴巴




#### 闭源
GPT系列 OpenAI - 应用：chatGPT

Claude系列 OpenAI离职人员 极高的上下文 claude-1:100K/claude-2:200K
使用地址：https://claude.ai/chats
PaLM系列 Google - 应用：Bard
https://ai.google/discover/palm2/

文心一言 百度

星火大模型 - 科大讯飞


### Langchain简介
产生于用api或者本地私有大模型构建应用的需求。是一个方便使用大模型的框架，其包含
* 模型输入/输出（Model I/O）：与语言模型交互的接口
* 数据连接（Data connection）：与特定应用程序的数据进行交互的接口
* 链（Chains）：将组件组合实现端到端应用。
* 记忆（Memory）：用于链的多次运行之间持久化应用程序状态；
* 代理（Agents）：扩展模型的推理能力。用于复杂的应用的调用序列；
* 回调（Callbacks）：扩展模型的推理能力。用于复杂的应用的调用序列；


https://github.com/langchain-ai/langchain

官方文档 https://python.langchain.com/docs/get_started/introduction
