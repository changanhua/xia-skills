# 快速开始指南

本指南将帮助你快速上手使用 xia-skills 仓库。

## 前置要求

- [Git](https://git-scm.com/) 已安装
- [GitHub](https://github.com/) 账号

## 使用已有 Skills

### 方式一：复制到项目

1. 克隆仓库：
   ```bash
   git clone https://github.com/changanhua/xia-skills.git
   ```

2. 找到需要的 skill 目录，例如：
   ```
   skills/review/review-design-docs/
   ```

3. 将 skill 复制到你的项目目录：
   - 如果你的项目已有 `.roo/skills/` 目录，直接复制整个 skill 文件夹
   - 如果没有，创建 `.roo/skills/` 目录后再复制

   ```bash
   # 示例：将 review-design-docs 复制到项目
   cp -r xia-skills/skills/review/review-design-docs 你的项目/.roo/skills/
   ```

4. 在 Roo Code Agent 中使用 skill

### 方式二：作为模板参考

如果你只想了解 skill 的设计思路，可以直接在 GitHub 上浏览 `SKILL.md` 文件，无需克隆。

## 创建新 Skill

如果你想贡献新的 skill，请参考 [Skill 规范说明](skill-spec.md)。

### 基本步骤

1. Fork 本仓库
2. 创建新分支：
   ```bash
   git checkout -b skill/your-skill-name
   ```

3. 在 `skills/` 目录下创建新的 skill 目录：
   ```
   skills/<category>/<skill-name>/
   └── SKILL.md
   ```

4. 编写 `SKILL.md` 文件
5. 提交并推送：
   ```bash
   git add .
   git commit -m "feat: 添加新skill"
   git push origin skill/your-skill-name
   ```

6. 创建 Pull Request

## 目录结构说明

```
xia-skills/
├── skills/                      # 技能目录
│   ├── review/                  # 审查类
│   │   ├── review-design-docs/
│   │   └── review-ai-friendly-design-docs/
│   ├── generate/                # 生成类（规划中）
│   └── common/                  # 通用类（规划中）
├── docs/                        # 文档
│   ├── getting-started.md
│   └── skill-spec.md
└── README.md
```

## 下一步

- 阅读 [Skill 规范说明](skill-spec.md) 了解更多细节
- 查看现有的 [Skills](SKILL_INDEX.md)
