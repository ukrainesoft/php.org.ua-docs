---
navigation:
  - function.trader-cdladvanceblock.html: « tradercdladvanceblock
  - function.trader-cdlbreakaway.html: tradercdlbreakaway »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradercdlbelthold
---
# tradercdlbelthold

(PECL trader >= 0.2.0)

tradercdlbelthold - Захоплення за пояс

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
