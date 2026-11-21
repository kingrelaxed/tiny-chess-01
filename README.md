# Tiny Chess

A deterministic Python chess engine for make.fun's `tiny-chess-01` bounty.
`main.py` is the complete runtime entry point and uses only Python's standard
library. It searches a fixed node budget with iterative-deepening alpha-beta,
capture ordering, and quiescence search.

The engine reads the current FEN and legal root moves from `MAKEFUN_ENV_URL`,
then sends its selected move back to the game environment. It makes no model
calls and uses no clock or randomness in its search.

To run it under the competition harness, use Python 3.13:

```sh
python3 main.py
```

The `main.py` file is packed from the readable engine source with the official
make.fun `compress` command. The source is not required at runtime.
