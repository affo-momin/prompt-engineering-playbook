# 🧩 Prompt Engineering Playbook

A practical, example-driven guide to writing prompts that get reliable answers from large language models,
plus a checklist for **evaluating** the responses. It comes from my work rating and comparing LLM responses
and from my Generative AI prompt engineering certification.

| File | What's inside |
|---|---|
| [prompt-patterns.md](prompt-patterns.md) | 8 core patterns, each with a weak prompt, a better prompt and why it works |
| [evaluation-checklist.md](evaluation-checklist.md) | The checklist I use to rate a response for accuracy, helpfulness, safety and instruction following |
| [rewrite-examples.md](rewrite-examples.md) | Before/after rewrites of real-world style prompts |

## The 5 rules I keep coming back to

1. **Say who it's for and why.** "Explain to a first-time voter" gets a better answer than "explain".
2. **Give the format up front.** Bullet count, table columns, word limit, JSON keys.
3. **Show, don't only tell.** One or two examples beat a paragraph of instructions.
4. **Split big jobs.** Ask for the outline first, then each part.
5. **Ask it to check itself.** "List any assumptions you made" surfaces weak spots.

## How to use this repo

- Copy a pattern from `prompt-patterns.md`, fill in the brackets and run it.
- Rate the answer with `evaluation-checklist.md`.
- If it scores low, find the closest case in `rewrite-examples.md` and apply the same fix.

## License

MIT. Free to use and adapt.
