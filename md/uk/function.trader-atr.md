Середній дійсний діапазон

-   [« traderatan](function.trader-atan.html)
    
-   [traderavgprice »](function.trader-avgprice.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Trader](ref.trader.md)
    
-   Середній дійсний діапазон
    

# traderatr

(PECL trader >= 0.2.0)

traderatr — Середній дійсний діапазон

### Опис

```methodsynopsis
trader_atr(    array $high,    array $low,    array $close,    int $timePeriod = ?): array
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