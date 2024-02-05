---
navigation:
  - function.trader-cdladvanceblock.md: « trader\_cdladvanceblock
  - function.trader-cdlbreakaway.md: trader\_cdlbreakaway »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_cdlbelthold
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_cdlbelthold

(PECL trader >= 0.2.0)

trader\_cdlbelthold - Захоплення за пояс

### Опис

```methodsynopsis
trader_cdlbelthold(    array $open,    array $high,    array $low,    array $close): array
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
