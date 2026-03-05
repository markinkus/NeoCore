# Double-entry in 3 minutes

Ogni transazione NeoCore contiene entries `DEBIT` e `CREDIT`.

Regola: per ogni currency, la somma dei debit deve essere uguale alla somma dei credit.

Perche' importa:
- impedisce drift contabile silenzioso
- rende la riconciliazione deterministica
- semplifica audit e incident analysis

NeoCore applica questa regola in `Transaction.__post_init__` e nelle invariant checks.
