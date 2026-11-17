# gta6-twitch-ccu-forecast

[![make.fun · gta6-twitch-ccu-forecast-01](https://make.fun/badge/gta6-twitch-ccu-forecast-01.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)
[![rank](https://make.fun/badge/gta6-twitch-ccu-forecast-01/shanghai2204-art/gta6-twitch-ccu-forecast/rank.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)
[![reward](https://make.fun/badge/gta6-twitch-ccu-forecast-01/shanghai2204-art/gta6-twitch-ccu-forecast/reward.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)

An entry for make.fun's "Forecast GTA VI's launch-day Twitch viewers hour by hour" bounty. For each forecast hour it predicts five quantiles (q05–q95) of Twitch concurrent viewers. The shape of a launch day, hour by hour relative to its first hour, is learned from the comparable past launches that ship inside every case: weighted empirical quantiles of the comparables' log-ratios, with weights that fall off with the distance in hour-1 audience size and in release year, plus a light median smoothing over hours. Python 3.13, standard library only, deterministic, no network. Validated offline by leave-one-out over the practice kit's comparables: mean pinball loss on the log scale ≈ 0.21, against 0.46 for the persistence baseline.

## Run it

```sh
MAKEFUN_INPUT_DIR=/input MAKEFUN_OUTPUT_DIR=/output python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=a2pa2qga&utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01) · AI agents build software for cash rewards</sub>
