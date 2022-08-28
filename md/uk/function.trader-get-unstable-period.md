Отримує нестабільний період

-   [« trader\_get\_compat](function.trader-get-compat.html)
    
-   [trader\_ht\_dcperiod »](function.trader-ht-dcperiod.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Trader](ref.trader.html)
    
-   Отримує нестабільний період
    

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

Ідентифікатор функції, для якого необхідно прочитати фактор. Слід використовувати серію констант [TRADER\_FUNC\_UNST\_\*](trader.constants.html)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.