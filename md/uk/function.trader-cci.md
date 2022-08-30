Індекс товарного каналу

-   [« traderbop](function.trader-bop.html)
    
-   [tradercdl2crows »](function.trader-cdl2crows.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Trader](ref.trader.md)
    
-   Індекс товарного каналу
    

# tradercci

(PECL trader >= 0.2.0)

tradercci - Індекс товарного каналу

### Опис

```methodsynopsis
trader_cci(    array $high,    array $low,    array $close,    int $timePeriod = ?): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`close`

Ціна закриття, масив реальних значень.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.