# Skill Index

本仓库包含以下可用的 Agent Skills：

## 审查类 Skills (Review)

### review-design-docs

- **描述**: 审查设计文档的完整性、详细程度、时效性、一致性、可实施性、技术栈稳定性和潜在风险点
- **适用场景**: 架构设计、技术方案、功能规范等文档的质量审查
- **路径**: `skills/review/review-design-docs/SKILL.md`

### review-ai-friendly-design-docs

- **描述**: 按照《面向低端AI模型的代码生成友好型设计文档编写指南》审查设计文档
- **适用场景**: 在AI代码生成前验证文档的"AI友好度"
- **路径**: `skills/review/review-ai-friendly-design-docs/SKILL.md`

---

## 分类说明

### 按功能分类

| 分类 | 说明 |
|------|------|
| review | 审查、检查类技能 |
| generate | 生成类技能（规划中） |
| debug | 调试类技能（规划中） |
| common | 通用类技能（规划中） |

---

## 使用方式

1. **本地使用**: 将目标 skill 目录复制到项目的 `.roo/skills/` 目录
2. **参考学习**: 阅读 SKILL.md 了解技能的设计思路
3. **贡献扩展**: 提交新的 skill 到本仓库

---

## 版本历史

- v0.1.0 (2026-02-27): 初始版本，包含2个审查类skills
