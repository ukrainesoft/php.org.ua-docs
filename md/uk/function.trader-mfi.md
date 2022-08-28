Індекс грошових потоків

-   [« trader\_medprice](function.trader-medprice.html)
    
-   [trader\_midpoint »](function.trader-midpoint.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Trader](ref.trader.html)
    
-   Індекс грошових потоків
    

# tradermfi

(PECL trader >= 0.2.0)

tradermfi - Індекс грошових потоків

### Опис

```methodsynopsis
trader_mfi(    array $high,    array $low,    array $close,    array $volume,    int $timePeriod = ?): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`close`

Ціна закриття, масив реальних значень.

`volume`

Обсяг торгів, масив реальних значень.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.