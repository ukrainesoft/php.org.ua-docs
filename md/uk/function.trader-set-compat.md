---
navigation:
  - function.trader-sarext.md: « tradersarext
  - function.trader-set-unstable-period.md: tradersetunstableperiod »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradersetcompat
---
# tradersetcompat

(PECL trader >= 0.2.2)

tradersetcompat — Встановлює режим сумісності

### Опис

```methodsynopsis
trader_set_compat(int $compatId): void
```

Встановлює режим сумісності, який впливає на спосіб виконання обчислень усіма функціями модуля.

### Список параметрів

`compatId`

Ідентифікатор сумісності. Використовується серія констант [TRADERCOMPATIBILITY](trader.constants.md)

### Значення, що повертаються

Функція не повертає значення після виконання.
