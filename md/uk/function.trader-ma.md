Ковзна середня

-   [« trader\_log10](function.trader-log10.html)
    
-   [trader\_macd »](function.trader-macd.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Trader](ref.trader.html)
    
-   Ковзна середня
    

# traderма

(PECL trader >= 0.2.0)

traderma — Ковзна середня

### Опис

```methodsynopsis
trader_ma(array $real, int $timePeriod = ?, int $mAType = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

`mAType`

Тип ковзної середньої. Слід використовувати серію констант [TRADER\_MA\_TYPE\_\*](trader.constants.html)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.