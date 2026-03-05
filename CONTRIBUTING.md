# Contributing

## Requirements
- Python 3.11+

## Quick start
```bash
python3.11 -m pip install ".[dev]"
python3.11 -m pytest -q
```

## Quality Gates
```bash
python3.11 -m pytest -q
python3.11 -m ruff check .
python3.11 -m mypy --strict .
```

## Development Rules
- Test-first: aggiungi test prima della feature.
- Runtime deps: solo stdlib obbligatoria.
- Importi: solo `Decimal` (mai float in input).
- Ledger: append-only, correzioni via nuove transazioni.
- Idempotenza: rispetta il comportamento di `LedgerEngine.post`.

## Good first issues
- Cerca issue con label `good first issue`, `help wanted`, `docs`.
- Backlog iniziale: [docs/issue-backlog.md](docs/issue-backlog.md).
