Встановлює нестабільний період

-   [« tradersetcompat](function.trader-set-compat.html)
    
-   [tradersin »](function.trader-sin.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Trader](ref.trader.md)
    
-   Встановлює нестабільний період
    

# tradersetunstableперіод

(PECL trader >= 0.2.2)

tradersetunstableperiod — Встановлює нестабільний період

### Опис

```methodsynopsis
trader_set_unstable_period(int $functionId, int $timePeriod): void
```

Впливає фактор нестабільного періоду для чутливих до нього функцій. Додаткову інформацію про нестабільні періоди можна знайти на сторінці документації API [» TA-Lib](http://ta-lib.org/d_api/ta_setunstableperiod.html)

### Список параметрів

`functionId`

Ідентифікатор функції, на яку має бути встановлений коефіцієнт. Серія констант [TRADERFUNCUNST](trader.constants.md) може використовуватися для на відповідну функцію.

`timePeriod`

Значення нестабільного періоду.

### Значення, що повертаються

Функція не повертає значення після виконання.