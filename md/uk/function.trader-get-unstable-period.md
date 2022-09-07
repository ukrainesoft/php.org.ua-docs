---
navigation:
  - function.trader-get-compat.md: « tradergetcompat
  - function.trader-ht-dcperiod.md: traderхтdcperiod »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradergetunstableперіод
---
# tradergetunstableперіод

(PECL trader >= 0.2.2)

tradergetunstableperiod — Отримує нестабільний період

### Опис

```methodsynopsis
trader_get_unstable_period(int $functionId): int
```

Отримує нестабільний коефіцієнт періоду конкретної функції.

### Список параметрів

`functionId`

Ідентифікатор функції, для якого необхідно прочитати фактор. Слід використовувати серію констант [TRADERFUNCUNST](trader.constants.md)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
