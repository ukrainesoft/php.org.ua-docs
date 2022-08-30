Середня ціна за період

-   [« tradermidpoint](function.trader-midpoint.html)
    
-   [tradermin »](function.trader-min.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Trader](ref.trader.html)
    
-   Середня ціна за період
    

# tradermidprice

(PECL trader >= 0.2.0)

tradermidprice — Середня ціна за період

### Опис

```methodsynopsis
trader_midprice(array $high, array $low, int $timePeriod = ?): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.