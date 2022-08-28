Параболічний SAR

-   [« trader\_rsi](function.trader-rsi.html)
    
-   [trader\_sarext »](function.trader-sarext.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Trader](ref.trader.html)
    
-   Параболічний SAR
    

# tradersar

(PECL trader >= 0.2.0)

tradersar - Параболічний SAR

### Опис

```methodsynopsis
trader_sar(    array $high,    array $low,    float $acceleration = ?,    float $maximum = ?): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`acceleration`

Коефіцієнт прискорення використовується максимального значення. Допустимий діапазон від 0 до [TRADER\_REAL\_MAX](trader.constants.html#constant.trader-real-max)

`maximum`

Коефіцієнт прискорення Максимальне значення. Допустимий діапазон від 0 до [TRADER\_REAL\_MAX](trader.constants.html#constant.trader-real-max)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.