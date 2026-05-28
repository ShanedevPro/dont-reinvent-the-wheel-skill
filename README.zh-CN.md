# Anti-Wheel Skill / 反重复造轮子 Skill

`reuse-before-build` 是一个通用 Agent Skill，用来提醒 AI 编程代理：在开始写自定义代码之前，先检查是否已经有成熟的现成方案。

这个 skill 的目的很简单：避免重复造轮子，减少不必要的复杂度，让项目更容易维护。

建议仓库名：

```text
anti-wheel-skill
```

## 包含内容

- `skills/reuse-before-build/SKILL.md`：正式的英文 skill 内容，供支持 `SKILL.md` 的 AI agent 读取和执行。
- `README.zh-CN.md`：中文开发者说明，也就是当前文件。
- `docs/skill-reference.zh-CN.md`：中文 skill 参考，解释这个原则应该如何使用。
- `docs/publish-to-github.zh-CN.md`：如何把这个压缩包发布到 GitHub 私有仓库。

## 什么时候使用

当你准备让 AI 开始构建新的功能、工具、库、集成、服务、UI 组件、工作流或自动化时，如果这件事可能已经有成熟方案，就应该先使用这个 skill。

## 核心原则

先找成熟方案，再决定是否自研。

优先选择“足够简单、足够成熟、能满足需求”的方案。只有当现有方案不适合、风险太高、成本太高、授权不合适，或者无法满足关键约束时，才应该写自定义实现。

## AI 在开始构建前应该回答

- 查过哪些已有方案？
- 推荐复用、改造、购买，还是自研？
- 为什么？
- 主要风险或取舍是什么？

## 注意

中文文档是给开发者阅读的说明材料，不是 skill 的正式执行内容。正式 skill 内容仍然是 `skills/reuse-before-build/SKILL.md`。

## 安装

这是一个 personal skill（直接放 `SKILL.md`），不是 Claude Code plugin。如果你想用 `/plugin install` 这种方式安装，需要额外做 plugin 打包。

把 `skills/reuse-before-build` 复制到你使用的 AI 编程工具的 skills 目录即可。

例如：

```sh
# Codex 风格目录
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R skills/reuse-before-build "${CODEX_HOME:-$HOME/.codex}/skills/reuse-before-build"

# Claude Code 风格目录
mkdir -p "$HOME/.claude/skills"
cp -R skills/reuse-before-build "$HOME/.claude/skills/reuse-before-build"
```

如果你的工具使用其他 skills 目录，保持 `reuse-before-build/SKILL.md` 这个结构不变即可。
