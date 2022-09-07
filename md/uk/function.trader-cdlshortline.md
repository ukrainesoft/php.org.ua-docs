---
navigation:
  - function.trader-cdlshootingstar.md: « tradercdlshootingstar
  - function.trader-cdlspinningtop.md: tradercdlspinningtop »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradercdlshortline
---
# tradercdlshortline

(PECL trader >= 0.2.0)

tradercdlshortline - Свічкова модель "Свічка короткої лінії"

### Опис

```methodsynopsis
trader_cdlshortline(    array $open,    array $high,    array $low,    array $close): array
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
