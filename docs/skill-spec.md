# Skill 规范说明

本文档定义了 xia-skills 仓库中 Skill 的编写规范。

## 文件结构

每个 Skill 必须包含以下文件：

```
<skill-name>/
└── SKILL.md          # 必需：Skill 定义文件
```

可选文件：

```
<skill-name>+
├── README.md         # 可选：详细说明文档
├── examples/         # 可选：示例目录
│   └── example.md
└── assets/           # 可选：资源目录
    └── diagram.png
```

## SKILL.md 格式

`SKILL.md` 是 Skill 的核心定义文件，必须遵循以下格式：

### 文件头（YAML Front Matter）

```yaml
---
name: skill-name           # Skill 名称（唯一，使用 kebab-case）
description: 简短描述     # 一句话说明（中文）
---
```

### 主要章节

| 章节 | 必需 | 说明 |
|------|------|------|
| # When to use | 是 | 何时使用此 Skill |
| # When NOT to use | 是 | 何时不使用此 Skill |
| # Inputs required from user | 是 | 用户需要提供的输入 |
| # Workflow | 是 | 执行步骤 |
| # Output format | 是 | 输出格式 |
| # Examples | 否 | 使用示例 |
| # Troubleshooting | 否 | 常见问题 |

### Workflow 格式建议

步骤应该清晰、可执行：

```markdown
## 步骤 1：xxx

1. 第一个子步骤
2. 第二个子步骤

## 步骤 2：xxx

1. 第一个子步骤
```

### 检查清单格式建议

当有多个检查项时，使用表格：

```markdown
| 检查项 | 说明 | 阈值 |
|--------|------|------|
| xxx    | xxx  | xxx  |
```

## 命名规范

| 类型 | 规则 | 示例 |
|------|------|------|
| Skill 名称 | kebab-case | `review-design-docs` |
| 目录名称 | kebab-case | `review-design-docs/` |
| 章节标题 | 中文标题 | `# When to use` |

## 分类规范

当前支持以下分类：

| 分类 | 说明 |
|------|------|
| `review/` | 审查、检查类技能 |
| `generate/` | 生成类技能（规划中） |
| `debug/` | 调试类技能（规划中） |
| `common/` | 通用类技能（规划中） |

新增分类需要更新 `SKILL_INDEX.md`。

## 版本管理

采用语义化版本（Semantic Versioning）：

```
v0.1.0
│ │ │
│ │ └── 补丁版本：文档修正、typo修复
│ └──── 次版本：新增可选字段、示例
└────── 主版本：破坏性变更（如SKILL.md结构变化）
```

## 验证清单

提交新的 Skill 前，请确认：

- [ ] `SKILL.md` 存在且格式正确
- [ ] YAML front matter 包含 `name` 和 `description`
- [ ] 包含必需的主要章节
- [ ] 命名符合规范
- [ ] 内容无明显的语法错误

---

## 参考示例

- [review-design-docs](../skills/review/review-design-docs/SKILL.md)
- [review-ai-friendly-design-docs](../skills/review/review-ai-friendly-design-docs/SKILL.md)
