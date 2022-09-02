---
navigation:
  - function.trader-cdldragonflydoji.md: « tradercdldragonflydoji
  - function.trader-cdleveningdojistar.md: tradercdleveningdojistar »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradercdlengulfing
---
# tradercdlengulfing

(PECL trader >= 0.2.0)

tradercdlengulfing - Модель поглинання

### Опис

```methodsynopsis
trader_cdlengulfing(    array $open,    array $high,    array $low,    array $close): array
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
