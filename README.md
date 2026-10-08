# web-design-taste

> Forked from [Alice59357/web-design-taste](https://github.com/Alice59357/web-design-taste) — 原始仓库仅 4 个 Markdown 文件，无任何可执行代码，已做安全审计。
> 在此基础上加了 WorkBuddy 用户专属的安装/使用说明，用于天真艾 / 瑶天真品牌页面设计。

一个 Claude Skill：帮**没有设计背景、不懂技术术语**的人做出设计师级的高质量网页。

你不需要会描述设计——用大白话说需求，从预设的风格卡片里做选择，用感受词（"太挤了""想要更高级一点"）给反馈，剩下的专业翻译工作全部由 Claude 完成。

## 它是怎么工作的

1. **人话访谈** — Claude 先问清楚：页面给谁看、希望对方看完做什么、你手上有什么素材
2. **选风格卡片** — 不让你凭空描述风格，而是给你 2-3 张匹配的风格卡片做选择题
3. **内部设计规划** — Claude 自己完成配色、字体、排版的专业决策
4. **产出完整网页** — 直接可运行的 HTML
5. **感受词迭代** — 你说"感觉太冷了"，Claude 翻译成具体的设计调整

## 安装

### 在 WorkBuddy 里安装（推荐）

WorkBuddy 把 skill 当作普通目录加载，从 `~/.workbuddy/skills/` 读。用户级安装一条命令搞定，跨项目可用：

```bash
git clone https://github.com/belonginin/web-design-taste.git \
  ~/.workbuddy/skills/web-design-taste
```

装好后重启 WorkBuddy，对它说"帮我做个网页 / 落地页 / 品牌官网 / 作品集"就会自动触发。

### 在 Claude Code 里安装（原版方式）

```bash
git clone https://github.com/Alice59357/web-design-taste.git \
  ~/.claude/skills/web-design-taste
```

重启 Claude Code 后同样可用。

### 在 Windows 上安装（多设备场景）

打开 PowerShell 或 Git Bash：

```powershell
git clone https://github.com/belonginin/web-design-taste.git "$env:USERPROFILE\.workbuddy\skills\web-design-taste"
```

重启 WorkBuddy 即可。

## 文件结构

```
web-design-taste/
├── SKILL.md                          # 主工作流
└── references/
    ├── style-cards.md                # 预设风格卡片库（7 张）
    ├── feeling-translation.md        # 感受词 → 设计参数翻译表
    └── tech-base.md                  # 技术基座规范
```

## 风格卡片速览

| # | 名字 | 一句话气质 |
|---|---|---|
| 1 | 苹果式 · 产品极简 | 一屏只说一件事，安静、笃定、贵 |
| 2 | Vogue · 杂志编辑风 | 像高级杂志跨页，有态度有立场 |
| 3 | 坂本龙一 · 静默留白 | 像乐谱休止符，每个字都在对的位置 |
| 4 | 暖光玻璃感 | 晨光透过磨砂玻璃，温暖有科技感 |
| 5 | 手作纸感 | 像用心做的手账，亲切诚恳有人味 |
| 6 | 暗色仪器感 | 精密仪器操作面板，专业锋利 |
| 7 | 明快转化型 | 每一屏都推着你往下走（销售页专用）