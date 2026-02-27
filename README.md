# xia-skills

集中管理 Roo Code Agent 技能模块的轻量级知识库。

## 概述

xia-skills 是一个用于存储和共享 Roo Code Agent 自定义技能的仓库。每个 skill 都是一个可复用的 Agent 行为模块，可以帮助自动化代码审查、文档生成等任务。

## 快速开始

### 使用已有 Skill

1. 克隆仓库到本地
2. 将需要的 skill 复制到项目的 `.roo/skills/` 目录
3. 在 Roo Code Agent 中使用 skill

### 贡献新 Skill

1. Fork 本仓库
2. 创建新分支
3. 添加你的 skill（遵循 [Skill 规范](docs/skill-spec.md)）
4. 提交 Pull Request

## 目录结构

```
xia-skills/
├── skills/                    # 技能目录
│   └── review/               # 审查类技能
│       ├── review-design-docs/
│       └── review-ai-friendly-design-docs/
├── docs/                      # 文档
│   ├── getting-started.md
│   └── skill-spec.md
└── README.md
```

## 可用 Skills

| Skill | 描述 |
|-------|------|
| [review-design-docs](skills/review/review-design-docs/) | 审查设计文档的完整性、详细程度、时效性等 |
| [review-ai-friendly-design-docs](skills/review/review-ai-friendly-design-docs/) | 审查设计文档的AI友好度 |

## 文档

- [快速开始指南](docs/getting-started.md)
- [Skill 规范说明](docs/skill-spec.md)
- [贡献指南](docs/contribute.md)（规划中）

## 许可证

MIT License - 详见 [LICENSE](LICENSE) 文件。
