---
navigation:
  - function.trader-cdl3blackcrows.md: « trader\_cdl3blackcrows
  - function.trader-cdl3linestrike.md: trader\_cdl3linestrike »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_cdl3inside
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_cdl3inside

(PECL trader >= 0.2.0)

trader\_cdl3inside - Три дні зсередини вгору і три дні зсередини вниз

### Опис

```methodsynopsis
trader_cdl3inside(    array $open,    array $high,    array $low,    array $close): array
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
