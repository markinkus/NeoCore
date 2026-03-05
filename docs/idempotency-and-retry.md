# Idempotency and retry

Sistemi reali ricevono eventi duplicati (retry, webhook, polling).

NeoCore usa `idempotency_key` in `LedgerEngine.post`:
- se la key non esiste, crea transaction + entries
- se la key esiste, ritorna la transaction originale
- nessun side-effect duplicato

Questo permette retry sicuri lato applicazione senza doppie scritture.
