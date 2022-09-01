---
navigation:
  - function.trader-cdlthrusting.html: « tradercdlthrusting
  - function.trader-cdlunique3river.html: tradercdlunique3river »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradercdltristar
---
# tradercdltristar

(PECL trader >= 0.2.0)

tradercdltristar - Свічкова модель "Трістар"

### Опис

```methodsynopsis
trader_cdltristar(    array $open,    array $high,    array $low,    array $close): array
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
