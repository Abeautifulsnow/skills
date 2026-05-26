# Skills

自用 Skills 集合 —— 面向 AI 编码助手的专业技能扩展。

## 目录结构

```
skills/
├── README.md
├── LICENSE
└── code-workflow/                        # 代码工作流编排 Skill
    ├── SKILL.md                          # 主编排器（5 步工作流）
    └── references/
        ├── code-reviewer/                # 代码审查子 Skill
        │   ├── SKILL.md                  # 审查流程与规范
        │   └── references/
        │       ├── rust.md               # Rust 专项审查指南
        │       ├── go.md                 # Go 专项审查指南
        │       ├── python.md             # Python 专项审查指南
        │       ├── typescript.md         # TypeScript/JS 专项审查指南
        │       ├── java.md               # Java 专项审查指南
        │       ├── react.md              # React 专项审查指南
        │       ├── nestjs.md             # NestJS 专项审查指南
        │       ├── vue.md                # Vue 3 专项审查指南
        │       ├── svelte.md             # Svelte 5 专项审查指南
        │       ├── code-quality-universal.md   # 通用代码质量反模式
        │       ├── code-review-best-practices.md # 审查最佳实践
        │       ├── common-bugs-checklist.md     # 常见 Bug 清单
        │       └── security-review-guide.md     # 安全审查指南
        ├── parallel-debugging/           # 并行调试子 Skill
        │   ├── SKILL.md
        │   └── references/
        │       └── hypothesis-testing.md
        └── git-commit/                   # Git 提交子 Skill
            └── SKILL.md
```

## 安装

将本仓库克隆到你的 AI 编码助手的 skills 目录。例如：

- **pi**：`~/.pi/agent/skills/`
- **Claude Code**：`~/.claude/skills/`

```bash
git clone https://github.com/Abeautifulsnow/skills.git ~/.pi/agent/skills
```

## 使用

当前包含一个完整的 **代码工作流编排 Skill (`code-workflow`)**，自动触发以下完整流程：

1. **获取变更背景** — 先理解"为什么改"
2. **代码审查** — 意图层 + 规范层双重审查，支持 9 种语言/框架
3. **调试修复** — 对发现的问题生成修复方案
4. **生成提交信息** — 符合 Conventional Commits 规范
5. **Git 操作指引** — 完整的 commit/push/PR 操作指引

触发关键词：`帮我看代码`、`review 一下`、`准备提交`、`生成 commit`、`走一下提交流程`。

### 语言/框架支持

| 语言/框架 | 专项审查指南 |
|-----------|-------------|
| Rust     | ✅ 含 cancel safety、spawn/await、unsafe 审查 |
| Go       | ✅ 含 goroutine 泄漏、context、错误处理 |
| Python   | ✅ 含 async/await、类型注解、性能优化 |
| TypeScript | ✅ 含 strict 模式、泛型、条件类型 |
| JavaScript | ✅ 沿用 TypeScript 规则 |
| Java     | ✅ 含 Record、虚拟线程、JPA N+1、Spring Boot |
| React    | ✅ 含 React 19 Actions、RSC、TanStack Query v5 |
| Vue      | ✅ 含 Vue 3.5 Reactive Props Destructure、defineModel |
| Svelte   | ✅ 含 Svelte 5 Runes、Load 函数、Form Actions |
| NestJS   | ✅ 含依赖注入、循环依赖、Use-Case Service |

通用指南：代码质量反模式、常见 Bug 清单、安全审查（OWASP Top 10）。

## License

MIT
