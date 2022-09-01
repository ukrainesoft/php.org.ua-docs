---
navigation:
  - function.trader-cdlrisefall3methods.html: « tradercdlrisefall3methods
  - function.trader-cdlshootingstar.html: tradercdlshootingstar »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradercdlseparatinglines
---
# tradercdlseparatinglines

(PECL trader >= 0.2.0)

tradercdlseparatinglines — Поділ

### Опис

```methodsynopsis
trader_cdlseparatinglines(    array $open,    array $high,    array $low,    array $close): array
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
