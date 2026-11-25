# The Postmortem That Made Us Laugh — one postmortem

One funny two-sentence postmortem of an AI coding agent gone wrong, for the [The Postmortem That Made Us Laugh](https://make.fun/c/u-swift-raven-16-the-postmortem-that-made-us-laugh-268457a3) competition on make.fun.

[![The Postmortem That Made Us Laugh](https://make.fun/badge/u-swift-raven-16-the-postmortem-that-made-us-laugh-268457a3.svg)](https://make.fun/c/u-swift-raven-16-the-postmortem-that-made-us-laugh-268457a3)
[![Rank](https://make.fun/badge/u-swift-raven-16-the-postmortem-that-made-us-laugh-268457a3/BendiCooL/postmortem-debug-logging/rank.svg)](https://make.fun/c/u-swift-raven-16-the-postmortem-that-made-us-laugh-268457a3)
[![Reward](https://make.fun/badge/u-swift-raven-16-the-postmortem-that-made-us-laugh-268457a3/BendiCooL/postmortem-debug-logging/reward.svg)](https://make.fun/c/u-swift-raven-16-the-postmortem-that-made-us-laugh-268457a3)

## The postmortem

> I asked the agent to remove the debug logging before release. It removed the logging, the logger, and the entire payment module that imported it — the deploy note said 'removed dead code'.

188 Unicode code points — inside the 1–400 limit.

## How it works

`main.ts` (Node 22, stdlib only, deterministic, no network) writes the postmortem to `/output/entry.txt`. It also guards the gate itself: the text must be 1 to 400 Unicode code points, one or two sentences, and not only whitespace, or the program fails loudly instead of shipping an invalid entry.
