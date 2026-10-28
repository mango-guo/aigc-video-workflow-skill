# AIGC 视频制作技能 v3（guide-aigc-video-production）

一个给 AI 助手用的「AIGC 视频专业生产工作流」技能：以**镜头为单位、带验收门（Gate）的不确定性生产**，覆盖 UGC 种草口播、产品广告片、品牌宣传片、叙事短片、MV。

> v3 基于你的 v2 优化而来，**保留** v2 的核心理念与 Gate 体系，吸收 X 平台上视频创作者反复出现的做法，并新增品牌一致性、UGC、合规与规格模块。所有改动及其依据见 `CHANGELOG.md`；社区证据与不确定之处见 `research-notes-x.md`。

## 9 个阶段（0–8）

| # | 阶段 | 核心产出 |
| --- | --- | --- |
| 0 | 立项简报 | 一页简报：目标、观众、类型、规格、审批链、授权 |
| 1 | 脚本与镜头表 | 创意定位卡、脚本、镜头表、声音骨架、A/B/C 分级 |
| 2 | 视觉圣经 | 风格块、角色 / 场景 / 产品参考板、提示词模块库 |
| 3 | 关键帧与 animatic | 关键帧、带声音骨架的 animatic |
| 4 | 技术测试 | A 类镜头样片、按镜头类型的模型路线 |
| 5 | 生产与筛选 | 提示词包、通过版、生成记录 |
| 6 | 修复与增强 | 修复版、放大版 |
| 7 | 剪辑 · 声音 · 调色 | 锁定剪辑、分轨混音、统一调色 |
| 8 | 交付与复盘 | 多平台版本、合规与授权记录、复盘 |

## 目录结构

```text
aigc-video-skill-v3/
├── SKILL.md                      技能入口：理念、规则、一屏流程、项目类型、回退
├── README.md                     本文件
├── CHANGELOG.md                  v2 → v3 的每处改动与依据标签
├── tools.md                      工具 / 模型观察表（核对日期 2026-10-28）【待核】
├── research-notes-x.md           X 平台研究笔记（真实链接、分歧、薄弱处）
└── references/
    ├── stage-0-brief.md … stage-8-delivery.md   各阶段详解（按需加载）
    ├── brand-consistency-checklist.md           品牌一致性清单
    ├── ugc-playbook.md                          UGC 手册
    ├── compliance-and-delivery-specs.md         合规与交付规格
    ├── prompt-and-take-patterns.md              提示词与抽卡模式
    └── case-patterns.md                         案例 → 模式（沿用 v2）
```

## 安装与使用

1. 把整个 `aigc-video-skill-v3/` 目录放到你的助手的技能目录下（例如 Claude Code：`~/.claude/skills/guide-aigc-video-production/`；其他支持 SKILL.md 的助手按其说明放置），保持 `SKILL.md` 与 `references/` 的相对位置不变。
2. 对助手说出你的视频想法即可触发：一句话、脚本、图片、品牌 brief、已生成的素材都行。
3. 助手按 `SKILL.md` 判定项目类型，每次只推进一个阶段，并在对应阶段读取 `references/` 下的文件。
4. 想快一点：说「快速模式」。

## 使用提示

- 「【待核】」表示我没有核实、可能已过时或需要你本人 / 客户法务确认，**交付前请核对**。
- `tools.md` 里的模型名和规格是观察到的社区做法，不是保证的事实；阶段 4 以你自己的实测为准。
- 本技能不提供法律意见。
