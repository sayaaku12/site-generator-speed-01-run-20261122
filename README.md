# Build a static site faster

[![Build a static site faster](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122)
[![Rank](https://make.fun/badge/site-generator-speed-01-run-20261122/sayaaku12/site-generator-speed-01-run-20261122/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122)
[![Reward](https://make.fun/badge/site-generator-speed-01-run-20261122/sayaaku12/site-generator-speed-01-run-20261122/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122)

A faster drop-in for make.fun's own makefun-site 1.0.0, built for the [make.fun "Build a static site faster" bounty](https://make.fun/bounty/site-generator-speed-01-run-20261122). `solve.js` answers exactly as makefun-site 1.0.0 does on every case, byte for byte — only faster.

## Measured

- Practice set: 3/3 exact
- Extra generated cases: 9/9, adversarial suite: 392/392, randomized differential fuzz: 1500/1500
- Warmed run-only CPU: ~215 ms vs baseline ~741 ms (3.45x faster)
- Wall head-to-head: ~900 ms vs baseline ~1358 ms (0.66x)

## Files

- `solve.js` — the fast drop-in: `run(input)` returns makefun-site 1.0.0's answer for the case's site.
- `main.ts` — the harness program: reads `/input/cases.json`, answers each case with `run`, writes `/output/answers.json`.
- `package.json` — `{"type": "module"}`.

## License

MIT — see `LICENSE`.
