# AIGC Aesthetic Definition Skill

> 把画面拆成可执行的美学参数，再写提示词。
> Turn an image idea into executable aesthetic parameters — then write the prompt.

一个给 AI 编码助手（Claude Code / Codex / DeepSeek Harness 等）用的技能包：写人物定妆照、三视图、剧照、场景图、视频首帧的提示词时，按「光 → 材质 → 风格 → 镜头」拆解，避免形容词堆叠和 AI 味。

## 解决什么问题 / What it fixes

- 画面「平」：没有光位，只有「电影感」
- 塑料感 / 像 CG：材质只写形容词，没有反射与缺陷
- 风格跑偏：混入插画、游戏、流派词，把写实拉成「画」
- 人物前后不是同一人：没有参考图与一致性锚点
- 可数特征数量错：九条尾巴画成一条

## 安装 / Install

```bash
git clone <this-repo> ~/.agents/skills/aigc-aesthetic-definition
```

或把整个目录复制到：

```
~/.agents/skills/aigc-aesthetic-definition/
```

Claude Code 用户也可放到 `~/.claude/skills/`。

## 内容 / What's inside

```
SKILL.md                    什么时候用、三要素、提示词骨架、四条铁律、快速诊断
references/light.md         光四维：光源/质感/光位/光色 + 情绪映射 + 写落点
references/material.md      材质写法 + 八个材质方向
references/styles.md        哪些风格能用、哪些一用就毁写实
references/formula.md       六种场景光影模块 + 镜头/胶片 + 视频写法
references/anti-patterns.md 勿用清单 + 15 个翻车点 + 9 项验收表
```

## 用法 / Usage

直接用自然语言提需求即可：

- 「给我写一个白璎夜戏的提示词」
- 「这张图发平，按美学定义诊断一下」
- 「这个风格词该不该加」

助手会加载本技能，按「主体 → 光 → 材质 → 镜头 → 画质 → 负面」输出可复制的整段提示词。

## 一条核心原则 / One rule

> **写物理，不写形容词。**
> Write physics, not adjectives.

不写「高级感」，写「单一 45° 柔光，5600K，光比 1:3，光落在鼻梁与颧骨」。

## 方法来源 / Attribution

框架参考傅炯《AIGC 提示词美学定义》（人民邮电出版社，2024）公开的方法论，并结合作者实践重写。

本技能为**独立整理**：非官方、未获授权、未收录原书文字与案例图。如需系统学习，请购买原书。

## License

MIT
