Плюс-спрямований індикатор

-   [« traderobv](function.trader-obv.html)
    
-   [traderplusdm »](function.trader-plus-dm.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Trader](ref.trader.html)
    
-   Плюс-спрямований індикатор
    

# traderplusді

(PECL trader >= 0.2.0)

traderplusdi — Плюс-спрямований індикатор

### Опис

```methodsynopsis
trader_plus_di(    array $high,    array $low,    array $close,    int $timePeriod = ?): array
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