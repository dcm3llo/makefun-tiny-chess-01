# Tiny Sentinel

Original MIT-licensed, standard-library-only Python 3.13 chess engine for
make.fun tiny-chess-01. Not derived from Sunfish or any other chess engine.

main.py contains the entire engine, packed by the competition kit's
makefun compress command. It reads no other repository file. Set
MAKEFUN_ENV_URL to the competition environment and run:

    python3 -P -s main.py

Search: deterministic iterative deepening, fixed 60,000-node budget,
0x88 legal move generation, alpha-beta/PVS, check-aware quiescence,
transposition bounds, history ordering, null-move pruning and late-move
reductions. Evaluation: material, phase-dependent king piece-square terms,
piece activity, bishop pair, pawn structure, passed pawns and open rook files.
Supports castling, en passant and all four promotions. Environment legal
moves constrain the root. Search accounts for game history and fifty moves.
No clock-based decisions, model calls, external dependencies or network
access beyond the supplied chess environment.

Tests and readable development source are retained outside the committed
snapshot to meet the 4,096-byte per-file and 8,192-byte repository limits.
The native build-session bundle carries the readable source and revisions.

No claim of optimal play or guaranteed contest qualification is made.
Local host timing is not a production-container performance guarantee.
