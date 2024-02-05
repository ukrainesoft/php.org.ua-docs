---
navigation:
  - function.trader-cdlshootingstar.md: « trader\_cdlshootingstar
  - function.trader-cdlspinningtop.md: trader\_cdlspinningtop »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_cdlshortline
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_cdlshortline

(PECL trader >= 0.2.0)

trader\_cdlshortline - Свічкова модель "Свічка короткої лінії"

### Опис

```methodsynopsis
trader_cdlshortline(    array $open,    array $high,    array $low,    array $close): array
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
