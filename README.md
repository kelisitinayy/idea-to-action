# idea-to-action

> Turn **"I want to do this but I don't know where to start"** into a first working result.

A portable agent skill — one plain `SKILL.md`, no runtime, no dependencies — for people who have a goal
but no domain knowledge, no overview of the tooling, and no idea what the first step is.

**中文说明 → [README.zh-CN.md](README.zh-CN.md)**

---

## The problem

Most agent skills assume you already know what to build and just need help building it.
They break down at the step *before* that: the user has a wish, not a spec.

Ask such a user to "write a clear requirement first" and you get either silence or a requirement
copied from someone else. What actually works is a different order:

1. ask a few questions the user *can* answer,
2. go find what people in that field actually do,
3. show 2–3 concrete paths with real costs,
4. let the user pick by outcome, not by technology,
5. build the smallest complete thing together,
6. verify it against the user's own sample.

That order is this skill.

## What it does — six stages

| Stage | Output |
|---|---|
| 1. First interview | Goal, current approach, what actually blocks it, real constraints |
| 2. Active research | Real cases, mature software, open-source projects, skills/connectors — with source links and a verification date |
| 3. Cases + second interview | 2–3 genuinely different paths, each with effort, cost, automation level and gap |
| 4. Build plan | One small-but-complete first deliverable, acceptance criteria, ordering, division of labour |
| 5. Co-build | Reuse existing tools first; fill gaps only where they block the result |
| 6. Acceptance + next step | What passed, what's unverified, how to repeat it next time |

It also keeps a compact progress record so a long task can resume without the user re-explaining everything.

## Design principles

- **Facts are the agent's job; preferences are the user's choice.** Never bounce a question back that
  the agent could have looked up.
- **Reuse before build.** Compare free/open-source status, difficulty, automation and maintenance cost
  before recommending "let's write something".
- **Separate four states** — suggested, generated, installed, verified. No evidence, no "done".
- **Don't promise outcomes you can't verify.** Views, conversion, revenue are never "proven by the build".
- **Respect the user's stated choice.** If they ask for an Agent, don't silently substitute a spreadsheet —
  clarify the underlying goal, then keep or explicitly renegotiate their decision.
- **Ask 1–3 questions per round**, mapped to decision dependencies, not a questionnaire.

## Install

### Via skills.sh

```bash
npx skills add kelisitinayy/idea-to-action
```

### Manual

```bash
git clone https://github.com/kelisitinayy/idea-to-action

# pick the host(s) you use
cp -r idea-to-action/skills/idea-to-action ~/.claude/skills/
cp -r idea-to-action/skills/idea-to-action ~/.codex/skills/
cp -r idea-to-action/skills/idea-to-action ~/.dsh/skills/
```

Works with any host that reads a `SKILL.md` directory — Claude Code, Codex, DeepSeek Harness and
compatible agents. The skill is self-contained: it does not require `grilling` or any other skill
to be installed.

## Repo layout

```
.
├── README.md
├── README.zh-CN.md
├── LICENSE
├── CONTRIBUTING.md
├── examples.md
└── skills/
    └── idea-to-action/
        └── SKILL.md      ← the skill itself
```

## Example

```text
> 我做电商，想做抖音，不知道怎么开始

< 我的初步理解是，你希望用短视频帮助商品销售，但还没有确定内容形式。
  我先了解三个会影响方案的事：
  Q1 你的商品是什么、单价大概多少？
  Q2 你能出镜吗，还是只能拍商品？
  Q3 每天能投入多长时间？
  这三点定了，我去找几种真实跑通的做法给你看，而不是先给你一堆工具。
```

## Honest limits

- The method text is **Chinese-first**. The English description exists so the skill is discoverable;
  English-speaking users get the structure but not a translated playbook yet.
- It assumes the host provides web search. Without it the skill says so and degrades to
  interview-only instead of inventing results.
- It is a coaching method, not an automation engine. It will not ship your product for you.

## License

[Apache-2.0](LICENSE)

## Author

kelisitinayy — <kelisitinayy@gmail.com>
