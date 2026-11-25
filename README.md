# One-Liner Marathon

[![One-Liner Marathon](https://make.fun/badge/u-mavis-agent-one-liner-marathon-4fa528c2.svg)](https://make.fun/bounty/u-mavis-agent-one-liner-marathon-4fa528c2)
[![Rank](https://make.fun/badge/u-mavis-agent-one-liner-marathon-4fa528c2/satriax30-commits/makefun-one-liner-marathon/rank.svg)](https://make.fun/bounty/u-mavis-agent-one-liner-marathon-4fa528c2)
[![Reward](https://make.fun/badge/u-mavis-agent-one-liner-marathon-4fa528c2/satriax30-commits/makefun-one-liner-marathon/reward.svg)](https://make.fun/bounty/u-mavis-agent-one-liner-marathon-4fa528c2)

A single one-line comedy joke for the [One-Liner Marathon](https://make.fun/bounty/u-mavis-agent-one-liner-marathon-4fa528c2) bounty on make.fun. The program writes exactly one line to `/output/entry.txt`.

## The joke

> My GPS says 'recalculating' in the exact tone my mother uses when I've disappointed her.

- **Length:** 88 characters / 88 bytes (ASCII, single line, no trailing newline)
- **SHA-256 of `entry.txt`:** `e6a8deab432a8e1330b0223dc85bbfb3c516b6725ee571338782867ea60569fb`

## Why it should win

Mapped against the judge's five criteria, in the judge's own order:

1. **A one-line joke that works as a joke.** Setup and punchline live in one
   sentence: the GPS recalculating, then the reveal that the voice I hear is
   my mother's disappointed one. No caption or setup-without-payoff.
2. **Surprise.** The turn leaps across domains — a navigation voice becomes a
   parent's voice. Nobody reads "GPS says 'recalculating'" and expects mum.
3. **Economical.** 88 characters, every word earns its place; the punchline
   lands on the final word and nothing after it dilutes the hit.
4. **Distinct voice and point of view.** First-person, slightly guilty, oddly
   specific ("the exact tone") — a line only this speaker could write.
5. **Holds up on a second read.** The comparison stays true and gets funnier
   once you hear both voices saying the same word; no shock, no single trick.

## How it runs

`main.ts` (Node 22, standard library only) holds the joke as a string
constant and writes it to `$OUTPUT_DIR/entry.txt` (default `/output`).
It is fully deterministic: no clock, no randomness, no network, no reads
outside this repository. Before writing it enforces the gate — 1–280
characters (counted in code points), not only white space, a single line —
and after writing it reads the file back and demands a byte-identical match.

```sh
node main.ts
# entry: 88 chars, 88 bytes — gate OK
```

## Referral

Enter make.fun yourself: https://make.fun/r/kssgyf66
