# CLAUDE.md — Death and Rememberance / Finding Lady Death

Guidance for Claude Code working in this repository. **Read this first, every session.**

## ⚖️ WORKFLOW LAW — READ EVERY SESSION (non-negotiable)

**We work ONLY on `main`. ALWAYS. This is Law.**

- There must be **NO other branch**, ever.
- Everything gets committed and pushed **straight to `main`**.
- Do **NOT** create feature branches. Do **NOT** create pull requests (not even drafts).
- If a cloud session starts on some other branch (e.g. `claude/...`), **push your work
  to `main` directly** so nothing splits off.
- The **only** exception is when the author (Terry) explicitly says otherwise for a task.

Git identity for commits:
```
git config user.email noreply@anthropic.com
git config user.name Claude
```

## What this repo is

Working repo for **Death and Rememberance / Finding Lady Death** (reincarnation dark fantasy). The book-editing tooling (Best Seller Studio `book-*`
agents, style/grammar gates) is configured per-environment/account, so it is available
here the same as in the sibling book repos.

The active project lives at `book/genesis/finding-lady-death/`; read its own `CLAUDE.md` and `STATE.yaml` first.

## 🔧 Pipeline source of truth — book-pipeline (READ + OBEY THE UPDATE RULE)

The book-writing pipeline (the 12 `book-*` agents, `/gemini` + `/grok` commands,
APODICTIC plugin) is shared from **`knightdx91-alt/book-pipeline`**, cloned into
`~/.claude/` each session by the environment setup script. It is the ONE place the
pipeline is edited.

**UPDATE RULE:** anytime you make the pipeline better — create a new book that needs
a new agent/tool, modify an agent/command/gate, or add a better entry to a shared
list (anti-AI pattern, craft-mistake rule, reusable motif convention, second-opinion
model) — commit that change to **book-pipeline** and push to `main`, so every book
inherits it next session. Do NOT strand improvements in a single book. (Per-book
style_check ALLOWLISTs are the exception — those stay in each book, seeded from the
_template.)
