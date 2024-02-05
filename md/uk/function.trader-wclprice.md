---
navigation:
  - function.trader-var.md: « trader\_var
  - function.trader-willr.md: trader\_willr »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_wclprice
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_wclprice

(PECL trader >= 0.2.0)

trader\_wclprice — Зважена ціна закриття

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
