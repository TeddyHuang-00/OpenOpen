# OpenOpen

> The only truly open project. Even being open is open to change.

[![License](https://img.shields.io/badge/license-whatever%20the%20PR%20says-blue)](LICENSE)

## Why

"Open" is the most abused word in software.

Some projects brand themselves "Open" while shipping proprietary models. Others call themselves "Open Source" but operate under a single corporation's CLA, a BDFL with ultimate veto, or a foundation whose board answers to paying members. Meanwhile, some of the most culturally open projects — modding communities, decompilation efforts — have no source code at all.

The common thread: **who decides what "open" means?** The answer is always someone in particular. Never everyone.

OpenOpen tries a different answer: **everyone, by vote, automatically.** No maintainers to convince. No steering committee to overrule. No CLA to sign. Just PRs, reactions, and a cron job.

## How it works

Every hour, a GitHub Action:

1. Fetches all open pull requests
2. Scores each by `(👍 + 1) / (👍 + 👎 + 2)` — Bayesian posterior mean of Beta(1,1) prior
3. Sorts descending
4. Attempts to merge the first conflict-free PR
5. If it merges, the loop stops. Next hour, rinse and repeat.

That's the entire governance model. No reviewers. No maintainers. No veto. Just votes and git.

If this workflow itself becomes unpopular, someone will PR a replacement — and if it gets more 👍 than the alternatives, it'll be replaced. The mechanism eats its own tail.

## FAQ

**What if someone PRs malicious code?**
Downvote it. If the community is asleep, well — that's democracy.

**What about the license?**
It's the [OpenOpen License](LICENSE) — no copyright, no liability, no restrictions. And yes, even the license itself can be replaced by PR. But the freedom of past contributions is irrevocable (see Section 4).

**Who owns this repo?**
Nobody. Or everybody. The answer is whatever the latest merged PR says it is.

**Is this a joke?**
Yes. And also no. Whether it stays a joke is also subject to PR.

**Is this legal?**
We waived liability in Section 2. You tell us.

## Getting started

```bash
git clone https://github.com/TeddyHuang-00/OpenOpen.git
# Change anything. Open a PR. Rally the 👍.
```

---

*Everything above this line — including this line — is subject to change by pull request. That's the point.*
