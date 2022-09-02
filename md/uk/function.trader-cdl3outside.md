---
navigation:
  - function.trader-cdl3linestrike.md: « tradercdl3linestrike
  - function.trader-cdl3starsinsouth.md: tradercdl3starsinsouth »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradercdl3outside
---
# tradercdl3outside

(PECL trader >= 0.2.0)

tradercdl3outside — Три зовнішні дні вгору і три зовнішні дні вниз

### Опис

```methodsynopsis
trader_cdl3outside(    array $open,    array $high,    array $low,    array $close): array
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
