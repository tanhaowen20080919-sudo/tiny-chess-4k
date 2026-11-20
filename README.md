# Eri Chess 4K

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/tanhaowen20080919-sudo/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/tanhaowen20080919-sudo/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 3,451 bytes of Python, built for the [tiny-chess-01 bounty on make.fun](https://make.fun/bounty/tiny-chess-01): the strongest engine that fits in 4 KB.

`main.py` is the readable source `engine.py` packed with make.fun's own `compress` tool. Inside: a 0x88 board, negamax alpha-beta search with a transposition table, quiescence search, PVS, king-tropism and passed-pawn evaluation, and repetition awareness across the game. It plays through the environment server protocol: it asks for a game, reads each FEN, and answers with a UCI move, searching to a fixed node budget so every run is deterministic.

Run it the way the bounty harness does: start the env server, set `MAKEFUN_ENV_URL` to its address, then `python3 main.py`.
