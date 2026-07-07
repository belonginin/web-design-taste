# web-design-taste

一个 Claude Skill：帮**没有设计背景、不懂技术术语**的人做出设计师级的高质量网页。

你不需要会描述设计——用大白话说需求，从预设的风格卡片里做选择，用感受词（"太挤了""想要更高级一点"）给反馈，剩下的专业翻译工作全部由 Claude 完成。

## 它是怎么工作的

1. **人话访谈** — Claude 先问清楚：页面给谁看、希望对方看完做什么、你手上有什么素材
2. **选风格卡片** — 不让你凭空描述风格，而是给你 2-3 张匹配的风格卡片做选择题
3. **内部设计规划** — Claude 自己完成配色、字体、排版的专业决策
4. **产出完整网页** — 直接可运行的 HTML
5. **感受词迭代** — 你说"感觉太冷了"，Claude 翻译成具体的设计调整

## 安装

把整个文件夹放进 Claude Code 的 skills 目录：

```bash
git clone https://github.com/Alice59357/web-design-taste.git ~/.claude/skills/web-design-taste
```

重启 Claude Code 后，对它说"帮我做个网页 / 落地页 / 作品集"就会自动触发。

也可以在 Claude 桌面端 / claude.ai 的 Skills 设置里上传这个文件夹。

## 文件结构

```
web-design-taste/
├── SKILL.md                          # 主工作流
└── references/
    ├── style-cards.md                # 预设风格卡片库
    ├── feeling-translation.md        # 感受词 → 设计参数翻译表
    └── tech-base.md                  # 技术基座规范
```
