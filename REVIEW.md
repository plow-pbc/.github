# Review instructions — .github

## Cause-first bug fixes

Fix a bug at its cause so the class can't recur. Never fix it with a layer, guard, link, workaround or hand-edit of data around it. A fix that adds net complexity must state why in the PR. When the bug comes from a duplicated source or identity, remove the duplicate rather than bridging the two.

Repo-specific reviewer policy. The universal review policy is prepended by the
reviewer and is not restated here.

## What this repo is

The plow-pbc organization's default community health files, currently the
pull-request template every org repo without its own inherits. No code.

**Stage:** internal. Read by the org's engineers and agents when they open PRs.

## Review bar

Report **Critical** and **Important** findings only. Nits and style go
unmentioned.

- **No security against coworkers.** Everyone with push access, and our own
  agents, are trusted. Do not propose guards or validation against them.
- **Simplest code wins.** Prefer deletion and inlining over new guards,
  fallbacks or abstractions for cases that cannot happen at this scale.

## Where the real risks are

- **Org-wide blast radius.** A template change lands on every plow-pbc repo
  that lacks its own; flag wording that contradicts a repo's own conventions
  or asks authors for something no reviewer checks.
