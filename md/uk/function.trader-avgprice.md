---
navigation:
  - function.trader-atr.md: « trader\_atr
  - function.trader-bbands.md: trader\_bbands »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_avgprice
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_avgprice

(PECL trader >= 0.2.0)

trader\_avgprice — Середня ціна

### Опис

```methodsynopsis
trader_avgprice(    array $open,    array $high,    array $low,    array $close): array
```

### Список параметрів

`open`

Ціна відкриття масив реальних значень.

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`close`

Ціна закриття, масив реальних значень.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
