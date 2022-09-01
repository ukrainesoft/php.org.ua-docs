---
navigation:
  - function.trader-var.html: « tradervar
  - function.trader-willr.html: traderwillr »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderwclprice
---
# traderwclprice

(PECL trader >= 0.2.0)

traderwclprice — Зважена ціна закриття

### Опис

```methodsynopsis
trader_wclprice(array $high, array $low, array $close): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`close`

Ціна закриття, масив реальних значень.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
