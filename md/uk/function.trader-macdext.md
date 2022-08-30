MACD з керованим типом MA

-   [« tradermacd](function.trader-macd.html)
    
-   [tradermacdfix »](function.trader-macdfix.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Trader](ref.trader.md)
    
-   MACD з керованим типом MA
    

# tradermacdext

(PECL trader >= 0.2.0)

tradermacdext - MACD з керованим типом MA

### Опис

```methodsynopsis
trader_macdext(    array $real,    int $fastPeriod = ?,    int $fastMAType = ?,    int $slowPeriod = ?,    int $slowMAType = ?,    int $signalPeriod = ?,    int $signalMAType = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`fastPeriod`

Номер періоду для швидкого ковзного середнього. Допустимі значення від 2 до 100000.

`fastMAType`

Тип ковзної середньої для швидкого ковзного середнього. Слід використовувати серію констант [TRADERМАTYPE](trader.constants.md)

`slowPeriod`

Номер періоду для повільного ковзного середнього. Допустимі значення від 2 до 100000.

`slowMAType`

Тип ковзної середньої для повільного ковзного середнього. Слід використовувати серію констант [TRADERМАTYPE](trader.constants.md)

`signalPeriod`

Згладжування сигнальної лінії (номер періоду). Допустимі значення від 1 до 100000.

`signalMAType`

Тип ковзної середньої сигнальної лінії. Слід використовувати серію констант [TRADERМАTYPE](trader.constants.md)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.