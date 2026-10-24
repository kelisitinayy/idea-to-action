# Examples / 示例

Three copy-paste prompts that show what `idea-to-action` is for — and what a good first reply looks like.
每个都是可以直接复制给 Agent 的原话。

---

## 1. 有目标、没有路径 / A goal with no path

```text
我做电商，想做抖音，不知道怎么开始。
```

**Expected first move** — not a tool list, not a 2000-word plan:

```text
我的初步理解是，你希望用短视频帮助商品销售，但还没有确定内容形式。
我先了解三个会直接影响方案的事：
  Q1 你的商品是什么、单价大概多少？
  Q2 你能出镜吗，还是只能拍商品？
  Q3 每天能投入多长时间？
这三点定了，我去找几种真实跑通的做法给你看，而不是先给你一堆工具。
```

The skill should *not* immediately recommend NLE software, a publishing tool, or an "AI content pipeline".

---

## 2. 用户要的是手段，不是结果 / The user names a technology, not an outcome

```text
给我搭一个全自动运营 Agent。
```

**Expected first move** — separate the outcome from the implementation:

```text
可以。但在动手前我想先确认一件事：你想减少的具体是哪部分工作？
  Q1 是内容生产、发布、还是数据复盘？
  Q2 现在这部分每周大概花你多少时间？
  Q3 如果只能自动化其中一件，你选哪件？
因为"全自动运营"覆盖的范围很大，其中有些环节目前能自动、有些必须人工把最后一道关，
我不想给你搭一个看着很酷但卡在发布环节的系统。
```

Then: research what's actually automatable today, show 2–3 paths with real limitations, and build one
end-to-end sample before promising anything "全自动".

---

## 3. 用户不想做选择 / The user refuses to choose

```text
我都看不懂，你帮我选。
```

**Expected behaviour** — recommend, explain by outcome and effort, and keep moving:

```text
好，我按你已知的条件选：走图文讲解这条，不做口播。
理由是它不需要出镜、制作时间最短、而且你现有的商品图可以直接用。
口播那条的效果上限更高，但要你先克服出镜和写稿两道坎，不适合作为第一版。
我先按这条做出第一条可审核的内容给你看，不满意再换。
```

It should not bounce the decision back, and it should not silently make irreversible moves either —
reversible work under existing authorization continues, real forks in direction get confirmed.

---

## What these examples are *not*

- Not fixed recommendations — the skill's own text says these are exploration examples, not a script.
- Not a guarantee of outcome. The skill explicitly refuses to promise views, conversion or revenue.
