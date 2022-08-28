Середній рейтинг індексу спрямованого руху

-   [« trader\_adx](function.trader-adx.html)
    
-   [trader\_apo »](function.trader-apo.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Trader](ref.trader.html)
    
-   Середній рейтинг індексу спрямованого руху
    

# traderadxr

(PECL trader >= 0.2.0)

traderadxr - Середній рейтинг індексу спрямованого руху

### Опис

```methodsynopsis
trader_adxr(    array $high,    array $low,    array $close,    int $timePeriod = ?): array
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