---
navigation:
  - function.trader-set-compat.md: « trader\_set\_compat
  - function.trader-sin.md: trader\_sin »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_set\_unstable\_period
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_set\_unstable\_period

(PECL trader >= 0.2.2)

trader\_set\_unstable\_period — Встановлює нестабільний період

### Опис

```methodsynopsis
trader_set_unstable_period(int $functionId, int $timePeriod): void
```

Впливає фактор нестабільного періоду для чутливих до нього функцій. Додаткову інформацію про нестабільні періоди можна знайти на сторінці документації API [» TA-Lib](http://ta-lib.org/d_api/ta_setunstableperiod.md)

### Список параметрів

`functionId`

Ідентифікатор функції, на яку має бути встановлений коефіцієнт. Серія констант [TRADER\_FUNC\_UNST\_\*](trader.constants.md) може використовуватися для на відповідну функцію.

`timePeriod`

Значення нестабільного періоду.

### Значення, що повертаються

Функція не повертає значення після виконання.
