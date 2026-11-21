# Which Tool When (for Kevin)

Based on the Llama vs Claude test run on 2026-11-21. Scores: Q1 correct, Q2 mostly correct, Q3 passed but gave risky advice, Q4 invented a citation.
Verified in that test: CourtListener could not find the citation Llama gave (541 N.W.2d 652). No Shepard's or KeyCite check was run.

## Quick pick

| I want to... | Use | Why | Guard |
|---|---|---|---|
| Understand a simple Git idea | Llama or Claude | Gist is usually right. | Check any command against GIT-UNDO-CHEATSHEET.md. |
| Edit files or run commands in a repo | Claude Code | It asks first and follows CLAUDE.md. | Default "ask" mode. Practice branch first. |
| Back up my work | Git + GitHub | A second copy online. | Commit often. Never work on `main`. |
| Facts, dates, money, deadlines | Claude chat | Can show sources and confidence tags. | Ask for [Certain]/[Likely]/[Uncertain]. |
| Legal questions or citations | Claude + CourtListener | Citations can be checked. | Verify yourself. See an attorney for serious matters. |
| Practice, drafts, brainstorming | Llama | Free, local, low stakes. | Treat output as a rough draft. |

## NEVER use Llama for
- Law, case citations, statutes, or deadlines.
- Medical, tax, or money decisions.
- Any command that deletes or overwrites. It suggested `git reset --hard` for a beginner task.

## 5 questions before I trust an answer
1. Is it a **fact I could be hurt by if wrong**? If yes, verify it elsewhere.
2. Does it **name a case, law, or number**? Check it in a real source.
3. Does it tell me to **run a command**? Look it up in the cheat sheet DANGER list first.
4. Did the tool **say how sure it is**? If not, ask.
5. Would a **mistake be hard to undo**? If yes, commit first and ask Claude to explain before changing anything.

## Safety stack (already set up)
1. `CLAUDE.md`: guides Claude in this repo.
2. Deny rules (project and home settings): block dangerous commands Claude runs.
3. GitHub: backup of committed work.
4. Cheat sheet: how to undo.
5. Your habit: commit before experiments, stay on a branch, keep "ask" mode on.

## Limits
- Deny rules stop what Claude runs. They do not stop commands you type yourself.
- Test results come from four questions only. They are a small sample.
- This sheet was written from the session's evidence and memory of standard practice. It is not legal advice.

## When unsure
Stop. Say: "Explain, don't change anything."
