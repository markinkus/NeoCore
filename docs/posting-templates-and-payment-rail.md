# Posting templates and payment rail

`TemplateEngine` applica template dichiarativi con ruoli account e regole entry.

Template builtin payment rail:
- `PAYMENT.AUTHORIZE`
- `PAYMENT.CAPTURE`
- `PAYMENT.SETTLE`
- `PAYMENT.REVERSE`

Reference scenario:
- `python -m neocore.scenarios.payment_rail`

Il vantaggio e' evitare posting manuali ripetitivi e ridurre errori di modellazione.
