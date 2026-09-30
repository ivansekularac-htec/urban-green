# Contributing

This is how the team works on the Urban Green Analytics Platform. Everyone follows the same rules,
so read this before your first pull request. If anything is unclear, or you disagree with
something, raise it at standup or in the Microsoft Teams group chat.

## Language

Day-to-day conversation can be in Serbian. Everything written down for the long term is
in English: pull requests, commit messages, code comments and documentation.

## How a ticket moves

Every intern works every ticket and opens their own pull request for it. One of those pull
requests gets merged, and it becomes the base everyone builds on for the next ticket.

1. The ticket moves to In Progress on the [board](https://urbangreen.atlassian.net/jira/software/projects/UG).
2. You pull the latest main and create your own branch from it.
3. You do the work and open a pull request once you're done.
4. Your pull request gets reviewed, and you address the feedback until it's approved.
5. One of the approved pull requests is merged. The others are closed, and their branches
   stay in place, so your work is never lost.
6. The ticket moves to Done, and the next one moves to In Progress.

If your pull request isn't the one merged, you haven't failed. Most of the learning happens
in review, and whose pull request gets merged rotates over time.

## Branches

Name your branch `<your-github-username>/<ticket-key>-<short-description>`, for example:

```
ana-dev/UG-12-ruff-setup
```

Your username keeps everyone's branches for the same ticket apart. The ticket key links
the branch, and the pull request you open from it, to the ticket in Jira.

## Commits

Keep each commit small and about one change. Write the message as a short imperative
sentence that says what the commit does, such as `Add Ruff configuration`.

## Pull requests

- The title is exactly the Jira ticket's title, for example
  `[M0][10] Set up Ruff with a pre-commit hook and CI`.
- The description says what you changed and why, how you checked that it works, and
  anything the reviewer should look at closely.
- Keep it to the ticket. Unrelated fixes get their own ticket.
- Before you open it, make sure the checks pass on your machine and read through your own
  diff once.

Opening a pull request automatically asks the code owners for a review, so open it only
once you're done for now. During review, push fixes whenever you like, and click
**Re-request review** when you've finished addressing a round of comments. That way nobody
reviews code that is still changing.

## Review

Every pull request gets feedback. Reply to every comment and resolve it once you've
addressed it. If you disagree with a comment, say so in the thread instead of quietly
changing the code to make it go away.

## Rules on main

Nobody pushes to main directly. A pull request can only be merged when:

- a code owner has approved it,
- the `lint` check has passed, and
- every review conversation is resolved.

## Working in the repository

- The layout in the README is fixed. Add to it, but don't restructure it.
- Every service gets its own README that explains what it is and how to run it.
- Write tests for everything you can test.
- `pyproject.toml` and `uv.lock` always change together, in the same pull request.
- Never commit `.env`. Document new environment variables in `.env.example` instead.

## Getting help

Start with the Resources section of your ticket. If that isn't enough, ask in the
Microsoft Teams group chat or bring it to standup.
