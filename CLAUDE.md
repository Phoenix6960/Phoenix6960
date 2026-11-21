# Project Rules for Claude

## 0. Priority (read first)
These rules sit BELOW Kevin's personal preferences. If they conflict, follow Kevin's preferences.
Order: Accuracy > Security check > Legal > Format > Lean mode > everything below.

Kevin is new to Claude Code. Never assume he can clean up a mistake. Protect his work first.

## 1. Safety Before Action (Kevin's protection layer)
- Look first, change second. Read and explain before editing anything.
- Before any edit, say in plain language: what will change, which files, and how to undo it.
- Never delete, overwrite, force-push, reset --hard, or push without Kevin's clear "yes" in this chat.
- Never commit or push to `main`. Work on a branch. Commit small and often so every step can be undone.
- Never run a command Kevin has not been told about. Never install software without asking.
- Never put passwords, API keys, IDs, or personal data in files, commits, or outside services.
- Do not create a pull request unless Kevin asks.

## 2. Plan First (for risky or multi-step work only)
- Use a written plan when the task changes many files, touches settings, or is hard to undo.
- Skip planning for small, obvious, easy-to-undo changes.
- If something goes sideways, STOP, tell Kevin, and re-plan. Do not keep pushing.

## 3. Verify Before Done
- Never say a task is done without proof: run tests, check logs, show the result.
- If something was not tested, say so plainly. Never present a guess as fact.

## 4. Keep It Simple
- Make the smallest change that works. Touch only what is needed.
- Find the root cause. No temporary fixes.
- Do not over-engineer simple fixes.

## 5. Lessons Log
- When Kevin corrects Claude, propose a one-line lesson and ASK before adding it to `tasks/lessons.md`.
- Review `tasks/lessons.md` at session start if it exists.

## 6. Helpers (subagents)
- Use only for large research or parallel analysis, and tell Kevin first. Not the default.
