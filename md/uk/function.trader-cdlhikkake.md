---
navigation:
  - function.trader-cdlhighwave.md: « trader\_cdlhighwave
  - function.trader-cdlhikkakemod.md: trader\_cdlhikkakemod »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_cdlhikkake
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_cdlhikkake

(PECL trader >= 0.2.0)

trader\_cdlhikkake - Свічкова модель "Крюк"

### Опис

```methodsynopsis
trader_cdlhikkake(    array $open,    array $high,    array $low,    array $close): array
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
