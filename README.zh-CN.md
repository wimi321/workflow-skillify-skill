# Workflow Skillify

[English](./README.md) | 简体中文

Use when a successful session or repeatable process should be captured as a reusable skill with steps, arguments, and invocation guidance.

## 这个技能是做什么的

Workflow Skillify 把 Claude Code 中可复用的一类工作流提取成独立 skill 仓库，方便在不同智能体环境里直接安装、复用和持续维护。

## 核心特点

- 聚焦单一能力边界，适合公开分发
- 仓库根目录就是 skill 根目录
- 内置 `agents/openai.yaml` 元数据
- 保留来源说明，便于追踪提取依据
- 提供中英文双语 README

## 擅长场景

- Turn a session into a reusable skill
- 执行 `SKILL.md` 中定义的标准工作流
- 为智能体或操作者提供稳定、可复用的输出

## 示例请求

- Turn this successful session into a reusable skill.
- Capture the process we just followed as a formal skill.

## 工作流程

1. Summarize the session and extract user-visible goals, corrections, and constraints.
2. Identify inputs, outputs, artifacts, and success criteria.
3. Interview for missing details only where the workflow is ambiguous.
4. Write a clean `SKILL.md` with trigger conditions, steps, and optional arguments.
5. Save the skill in the appropriate repo-level or personal location.

## 输入

- Session history
- User corrections
- Desired save scope

## 输出

- Reusable SKILL.md
- Trigger and argument guidance

## 成功标准

- The resulting skill captures the real workflow.
- User corrections are preserved as rules.
- The saved skill is specific and reusable.

## 不适用场景

- Over-interviewing simple workflows
- Saving a vague process with no triggers or success criteria

## 安装方式

### 作为独立 skill 使用

克隆本仓库，并将仓库根目录放入兼容的 skill 目录即可。

### 从合集仓库使用

该 skill 也收录在总仓库中：

- [claude-code-skills-extract](https://github.com/wimi321/claude-code-skills-extract)

## 仓库结构

- `SKILL.md`：技能主定义
- `README.md`：英文说明
- `README.zh-CN.md`：中文说明
- `agents/openai.yaml`：面向智能体 UI 的元数据
- `references/`：来源与补充说明
- `LICENSE`：开源许可证

## 来源说明

Derived from `src/skills/bundled/skillify.ts`.

## 相关项目

- 总仓库：[claude-code-skills-extract](https://github.com/wimi321/claude-code-skills-extract)
- 当前仓库：[workflow-skillify-skill](https://github.com/wimi321/workflow-skillify-skill)
