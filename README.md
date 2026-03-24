# Upstream Narrative Package Protocol Specification
# 上游镜核叙事数据包协议文本规范

A protocol specification for translating narrative input into structured narrative packages.  
This project treats the **narrative package itself as a final product**, not merely as an intermediate artifact before chapter generation.

一套用于将叙事输入转译为结构化叙事数据包的协议文本规范。  
本项目将**叙事数据包本身视为目标产物**，而不只是章节生成之前的中间材料。

---

## Overview ｜ 项目概览

This repository presents the public overview edition of an upstream narrative package protocol.  
Its purpose is to define how natural-language narrative input is translated into a structured, bounded, and reusable narrative package.

本仓库展示的是一套上游叙事数据包协议的公开概览版。  
其目标是定义：如何将自然语言叙事输入，转译为**结构化、低歧义、可复用**的叙事数据包。

This project is **not**:

- a writing assistant
- a free-form story generator
- a chapter generation tool
- a general-purpose text summarizer

本项目**不是**：

- 写作助手
- 自由创作器
- 章节生成工具
- 通用文本摘要器

It is an **upstream protocol specification** for narrative structuring.

它是一份面向**上游叙事结构转译**的协议文本规范。

---

## Positioning ｜ 项目定位

The protocol is designed for the upstream stage of a narrative workflow.

Its responsibility is to:

- read the current narrative input
- identify directly supported information
- organize that information into a structured narrative package
- update a boundary summary for later reference

该协议定位于叙事工作流的上游阶段。

它的职责是：

- 读取当前叙事输入
- 识别当前文本中可直接成立的信息
- 将信息整理为结构化叙事数据包
- 更新可供后续章节参考的边界摘要

It does **not**:

- generate chapter prose
- expand missing content
- invent worldbuilding
- treat historical summaries as current evidence

它**不**负责：

- 生成章节正文
- 补全缺失内容
- 新增世界观设定
- 将历史摘要当作本章证据

---

## Product Goal ｜ 产品目标

The core product goal of this specification is:

> to make the narrative package itself a stable, inspectable, and reusable final output.

本协议当前的核心产品目标是：

> 让叙事数据包本身成为一种稳定、可检查、可复用的最终产物。

This means the package can exist independently as:

- an archival unit
- a testing object
- a comparison target across protocol versions
- a continuity reference layer
- a standard interface for downstream or adjacent systems

这意味着，叙事数据包可以独立作为：

- 存档单元
- 测试对象
- 协议版本对比对象
- 连续性参照层
- 下游系统或相邻系统的标准接口

Downstream chapter generation is only **one possible application** of the package, not its sole purpose.

下游章节生成只是叙事数据包的**一种应用方向**，不是它存在的唯一目的。

---

## Inputs ｜ 输入

The current protocol accepts two input sources:

1. Boundary Summary from previous context  
2. Author-provided natural-language text for the current chapter

当前协议面向两类输入：

1. 上文规则边界摘要  
2. 当前章节作者自然语言文本

---

## Outputs ｜ 输出

The protocol produces two outputs:

1. Narrative Package  
2. Updated Boundary Summary

协议输出两部分内容：

1. 叙事数据包  
2. 更新后的上文规则边界摘要

---

## Narrative Package Structure ｜ 叙事数据包结构

The narrative package uses a three-layer structure:

叙事数据包采用三层结构：

### L1 World Rules ｜ L1 世界规则

Used to record anomalous facts directly established in the current chapter text.

Examples:

- anomalous phenomena
- confirmed abilities
- anomalous equipment
- anomalous individuals
- spatial anomalies

用于记录当前章节文本中**直接成立的异常事实**。

例如：

- 异常现象
- 已成立能力
- 异常装备
- 异常个体
- 空间异常

**Constraint ｜ 约束**  
L1 only records what is directly supported by the current text.  
Historical boundary summaries are not treated as current-chapter evidence.

L1 仅收录当前文本可以直接支撑的异常事实。  
历史边界摘要不能视为本章直接证据。

---

### L2 Narrative Skeleton ｜ L2 叙事骨架

Used to organize the structural backbone of the current chapter.

Examples:

- chapter type
- roles
- role relations
- scenes
- time nodes
- event chains
- core conflict
- chapter goal
- progression points
- suspense

用于整理当前章节的结构主干。

例如：

- 章节类型
- 角色
- 角色关系
- 场景
- 时间节点
- 事件链
- 核心冲突
- 章节目标
- 推进点
- 悬念

---

### L3 Narrative Texture ｜ L3 叙事血肉

Used to preserve perceptual and expressive material from the current chapter.

Examples:

- emotion / motivation → action links
- strong visual anchors
- original author lines
- rhythmic phrases
- slogan-like expressions
- distinctive expressive traces

用于保留当前章节中的感知层与表达层信息。

例如：

- 情绪 / 动机 → 行动链
- 强画面锚点
- 作者原句
- 节奏句
- 口号式表达
- 高辨识表达痕迹

---

## Core Principles ｜ 核心原则

The current freeze-oriented direction of the protocol follows these principles:

当前冻结方向下，本协议遵循以下核心原则：

### 1. No new setting injection ｜ 不新增设定
The protocol must not invent worldbuilding, mechanisms, relationships, or facts not directly supported by the input text.

协议不得编造输入文本中未直接出现的设定、机制、关系或事实。

### 2. No completion of missing information ｜ 不补全未出现信息
If something does not appear in the current text, it should not be automatically completed.

凡当前文本未出现的信息，不得自动补全。

### 3. Historical summaries are reference-only ｜ 历史摘要仅作参照
The boundary summary from previous context may be used as a reference layer, but not as direct evidence for the current chapter.

上文规则边界摘要只能作为参照层使用，不能直接替代本章证据。

### 4. L1 only records directly established anomalous facts ｜ L1 仅收当前文本直接成立的异常事实
The L1 layer is restricted to anomaly-related facts directly established in the current text.

L1 层只允许收录当前文本中直接成立的异常事实。

### 5. Structural classification over literary interpretation ｜ 结构归类优先于文学解释
The protocol extracts and organizes; it does not perform literary commentary or thematic interpretation.

协议负责抽取与归类，不负责文学评论或主题阐释。

### 6. Distinctive author expressions should be retained ｜ 高辨识表达应尽量保留
Original lines and highly identifiable expressions should be preserved whenever they carry execution value.

当原句或高辨识表达具有执行价值时，应尽量保留。

---

## Boundary Summary ｜ 上文规则边界摘要

After the current chapter is translated, the protocol produces an updated boundary summary based on the chapter result.

This summary serves as a reference layer for later chapters, but it does not replace current-chapter textual evidence.

协议在完成本章转译后，会基于本章结果生成更新后的上文规则边界摘要。

该摘要用于后续章节作为参照层使用，但不能替代当前章节的直接文本证据。

Its role is continuity control, not retroactive proof.

它的作用是连续性控制，而不是反向充当证据来源。

---

## Why This Protocol Exists ｜ 为什么要做这个协议

Narrative systems often fail not because they cannot produce text, but because they cannot keep boundaries stable.

This specification is designed to reduce:

- unauthorized expansion
- evidence drift
- confusion between current facts and historical memory
- unstable narrative interfaces
- uncontrolled interpretation in later stages

很多叙事系统的问题，不是“写不出来”，而是“边界守不住”。

本协议的价值在于压低以下风险：

- 越权扩写
- 证据漂移
- 当前事实与历史记忆混淆
- 叙事接口不稳定
- 后续阶段的失控解释

The upstream goal is not maximal creativity.  
The upstream goal is a stable narrative interface.

上游阶段的目标不是最大化创造性。  
上游阶段的目标是建立一个稳定的叙事接口层。

---

## Relationship to Downstream Systems ｜ 与下游系统的关系

This repository focuses on the upstream protocol only.

Its outputs may be consumed by downstream or adjacent systems such as:

- chapter generation protocols
- consistency checking tools
- narrative analysis workflows
- editing pipelines
- structured archival systems

本仓库只聚焦上游协议本身。

其输出结果可以被下游系统或相邻系统消费，例如：

- 章节生成协议
- 一致性校验工具
- 叙事分析工作流
- 编辑流程
- 结构化归档系统

A downstream chapter generator is only one consumer of this package format.

下游章节生成器，只是这种数据包格式的一个消费端。

---

## Public Scope ｜ 当前公开范围

This public repository currently includes:

- protocol overview
- example results
- iteration traces
- version markers
- revision notes

本公开仓库当前展示内容包括：

- 协议概览
- 案例结果
- 运行轮次
- 版本痕迹
- 迭代备注

---

## Non-Public Scope ｜ 当前未公开范围

The following materials are not fully disclosed in this public repository:

- full runtime text
- complete field definitions
- full decision thresholds
- complete constraint rules
- complete forbid lists
- detailed execution rules

以下内容当前不在公开仓库中完整展示：

- 完整运行文本
- 全量字段细则
- 全部判定阈值
- 全部约束规则
- 全部禁止项
- 详细执行细则

---

## Current Status ｜ 当前状态

**Project Name / 项目名称**  
Upstream Narrative Package Protocol Specification  
上游叙事数据包协议文本规范

**Current Version / 当前版本**  
v1.3

**Edition / 文件类型**  
Public Overview Edition  
公开概览版

**Current Track / 当前轨道**  
Freeze-oriented iteration  
冻结方向持续迭代

**Historical Internal Label / 历史内部编号**  
Module 4  
模块4

---

## Intended Use ｜ 适用用途

This specification is currently suitable for:

- narrative package production
- chapter-to-package conversion tests
- package comparison across versions
- continuity-boundary referencing
- upstream/downstream interface design
- protocol-oriented narrative workflow experiments

本协议文本规范当前适用于：

- 叙事数据包生产
- 完整章节转数据包测试
- 跨版本数据包对比
- 连续性边界参照
- 上下游接口设计
- 协议化叙事工作流实验

---

## Not Intended For ｜ 非目标用途

This repository is not intended as:

- a free-writing AI system
- a general-purpose summarizer
- a literary interpretation framework
- a direct chapter generation product
- an automated story completion system

本仓库并非以下用途的目标产品：

- 自由写作型 AI 系统
- 通用摘要器
- 文学解释框架
- 直接章节生成产品
- 自动补全剧情系统

---

## One-Sentence Summary ｜ 一句话总结

This project defines an upstream protocol specification that treats the narrative package itself as a reusable final product.

本项目定义了一套上游协议文本规范，将叙事数据包本身视为可复用的最终产物。

联系方式

如对协议思路、案例结构或合作方向有明确交流意向，可通过以下邮箱联系：

185555045@qq.com
jiaowodawa8@gmail.com
