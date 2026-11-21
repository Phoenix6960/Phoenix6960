# Git Undo Cheat Sheet (for Kevin)

Source: written from memory of standard Git practice, not verified against Git docs this session.
Test every command in a throwaway repo first.

## Golden rules
1. **Commit before you experiment.** A commit is a save point.
2. **Work on a branch, never on `main`.**
3. **Look before you act.** Run `git status` first.
4. **If unsure, stop and ask Claude.** Do not guess at commands.

## Look (safe, changes nothing)

| I want to... | Command |
|---|---|
| See what changed | `git status` |
| See the exact edits | `git diff` |
| See save-point history | `git log --oneline` |
| See which branch I'm on | `git branch --show-current` |

## Undo (match your situation)

| Situation | Command | Safe? |
|---|---|---|
| I edited a file and want the old version back | `git restore FILE` | **Loses your edits for that file.** |
| I staged a file by mistake (`git add`) | `git restore --staged FILE` | Safe. Edits stay. |
| I deleted a file by accident (not committed) | `git restore FILE` | Safe. |
| My last commit was wrong, NOT pushed yet | `git reset --soft HEAD~1` | Safe. Edits stay. |
| A commit was already pushed and is wrong | `git revert COMMIT_ID` | Safe. Adds an "undo" commit. |
| I need to set work aside for a moment | `git stash` (back: `git stash pop`) | Safe. |
| I want to try something risky | `git switch -c experiment` | Safe. Leaves `main` alone. |
| I want to go back to my main work | `git switch main` | Safe. |

## DANGER list: never type these without asking Claude first
- `git reset --hard`: erases uncommitted work.
- `git push --force`: can overwrite other copies online.
- `git clean -fd`: deletes untracked files for good.
- `git checkout .` or `git restore .`: discards ALL uncommitted edits.
- `rm -rf`: deletes folders for good.

## Panic plan
1. Stop. Do not type more commands.
2. Run `git status` and `git log --oneline`.
3. Paste the output to Claude and say "explain, don't change anything."
4. Commits pushed to GitHub are a backup. Your work is usually recoverable.

## Words
- **Commit:** a saved snapshot of your files.
- **Branch:** a separate line of work.
- **Push:** send your commits to GitHub.
- **Stage:** mark a file to go into the next commit.
