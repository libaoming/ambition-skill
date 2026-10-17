# ambition — 把任务往大了做

一个 Claude Code / Agent Skill。它用三个方法改写你交给模型的任务，让模型做得更深、更有用：

- **高度**：交结果，不交步骤。先找到这件事最终服务的决定。
- **深度**：像顶尖专家一样做。从原始材料开始，用行业真正的工具，并找一个模型以外的裁判来验证结果。
- **广度**：换几个领域的眼睛看同一件事，并且一定有一个红队专门论证结论会错。

方法来自 Felix Rieseberg 的文章 [How to Be More Ambitious: A Tutorial for Humans with Models](https://felixrieseberg.com/how-to-be-more-ambitious-a-tutorial-for-humans-with-models/)。本仓库是**非官方改编**，与作者和 Anthropic 无关。

在原文之外，本技能加了几条实践中踩坑得来的规则：

- 外部数据当裁判前，先过三项检查：**独立**（没有循环论证）、**干净**（没有刷量和口径混用）、**同一批人**（数据背后是你关心的用户）。不过就降级为「参考」。
- 原始材料还不存在时，把任务改成先建采集。
- 交付前交给一个没参与写作的子 agent 核数字、挑刺；被推翻的结论要点名说出来。

## 安装

```bash
git clone https://github.com/libaoming/ambition-skill.git
cp -r ambition-skill/ambition ~/.claude/skills/
```

## 使用

两种用法：

- **只改写**：「用 ambition 改写这个 prompt：……」。走第 1–3 步，交出一份可以直接执行的改写稿。
- **改写并执行**：「往大了做：调研 X」。走完 5 步：高度 → 深度 → 广度 → 执行 → 过外部裁判和红队。

技能正文是中文。

## English

`ambition` is an Agent Skill (Chinese) that rewrites a task along three axes from Felix Rieseberg's essay *How to Be More Ambitious*: **altitude** (delegate the outcome, not the task), **depth** (raw sources, expert tools, an outside judge), and **range** (several disciplines plus a red team). It adds a few field-tested rules: vet external data for independence, cleanliness and audience fit before using it as a judge; build collection first when raw data doesn't exist yet; and have an independent sub-agent recheck numbers and red-team the result before delivery. Unofficial adaptation, not affiliated with the author or Anthropic.

## License

MIT
