Потрійна експоненційна ковзна середня

-   [« tradersum](function.trader-sum.html)
    
-   [tradertan »](function.trader-tan.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Trader](ref.trader.html)
    
-   Потрійна експоненційна ковзна середня
    

# traderтз

(PECL trader >= 0.2.0)

tradert3 - Потрійна експоненційна ковзна середня

### Опис

```methodsynopsis
trader_t3(array $real, int $timePeriod = ?, float $vFactor = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

`vFactor`

Коефіцієнт обсягу. Допустимі значення від 1 до 0.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.