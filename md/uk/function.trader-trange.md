---
navigation:
  - function.trader-tema.md: « trader\_tema
  - function.trader-trima.md: trader\_trima »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_trange
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_trange

(PECL trader >= 0.2.0)

trader\_trange — Справжній діапазон

### Опис

```methodsynopsis
trader_trange(array $high, array $low, array $close): array
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
