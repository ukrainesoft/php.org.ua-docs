---
navigation:
  - function.trader-get-compat.md: « trader\_get\_compat
  - function.trader-ht-dcperiod.md: trader\_ht\_dcperiod »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_get\_unstable\_period
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_get\_unstable\_period

(PECL trader >= 0.2.2)

trader\_get\_unstable\_period — Отримує нестабільний період

### Опис

```methodsynopsis
trader_get_unstable_period(int $functionId): int
```

Отримує нестабільний коефіцієнт періоду конкретної функції.

### Список параметрів

`functionId`

Ідентифікатор функції, для якого необхідно прочитати фактор. Слід використовувати серію констант [TRADER\_FUNC\_UNST\_\*](trader.constants.md)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
