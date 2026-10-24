# Contributing

This is a single-file agent skill. Contributions are welcome, but the bar is deliberately narrow:
the skill is a **method**, not a feature list. Adding a checklist item is easy; keeping the method
coherent is the hard part.

## What's genuinely useful

- **A failing case.** A real conversation where the skill made a bad move — asked a question it could
  have looked up, dumped a tool list instead of a path, promised a result it couldn't verify. Paste the
  transcript, say what should have happened.
- **A host-compatibility fix.** The skill should work on Claude Code, Codex, DeepSeek Harness and any
  host that reads `SKILL.md`. If it assumes a capability a host doesn't have, that's a bug.
- **A translation.** The method text is Chinese-first. A careful English translation of `SKILL.md`
  is the single highest-value contribution right now.

## What will probably be declined

- Adding new stages or gates. Six stages is already at the limit; more structure makes it a questionnaire.
- Turning it into an automation pipeline. It's a coaching method.
- Long tool lists or vendor recommendations. The skill explicitly avoids recommending before researching.

## How to submit

1. Open an issue describing the failing case or the gap. Transcripts beat opinions.
2. For changes to `SKILL.md`, keep the diff small and explain which principle it serves.
3. Don't reformat unrelated sections — it makes review impossible.

## Ground rules for the method

Two invariants will not be traded away:

- **Facts are the agent's job, preferences are the user's choice.** Any change that pushes fact-finding
  onto the user is a regression.
- **No evidence, no "done".** The four states — suggested / generated / installed / verified — stay separate.

## License

By contributing you agree your contribution is licensed under [Apache-2.0](LICENSE).
