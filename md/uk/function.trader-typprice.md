---
navigation:
  - function.trader-tsf.md: « trader\_tsf
  - function.trader-ultosc.md: trader\_ultosc »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_typprice
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_typprice

(PECL trader >= 0.2.0)

trader\_typprice — Типова ціна

### Опис

```methodsynopsis
trader_typprice(array $high, array $low, array $close): array
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
