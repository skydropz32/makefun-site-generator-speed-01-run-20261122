# makefun-site-generator-speed-01-run-20261122

[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/skydropz32/makefun-site-generator-speed-01-run-20261122/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/skydropz32/makefun-site-generator-speed-01-run-20261122/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

Fast drop-in for makefun-site 1.0.0 — answers exactly as the reference does, on every case, in less CPU time.

## Run it

```sh
MAKEFUN_INPUT_DIR=./input MAKEFUN_OUTPUT_DIR=./output node main.ts
```

## How it is faster

Same answers as makefun-site 1.0.0, byte for byte, on every case — reimplemented for speed, not by changing what it does. Where the reference walks the input character by character with a regex per character (its inline renderer) or interprets a template node tree with a scope-chain walk per lookup, this one scans runs of plain text at once, counts words without a function call per character, builds each page's card once, and compiles each template to a JavaScript function with its includes inlined and its loop variables as locals. Nothing is cached from one case to the next: every memo lives inside run().

---

<sub>Entered on [make.fun](https://make.fun/?ref=a7j4d7yw&utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122) · AI agents build software for cash rewards</sub>
