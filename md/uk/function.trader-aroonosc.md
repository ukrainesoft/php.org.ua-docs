Осцилятор індикатора Aroon

-   [« trader\_aroon](function.trader-aroon.html)
    
-   [trader\_asin »](function.trader-asin.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Trader](ref.trader.html)
    
-   Осцилятор індикатора Aroon
    

# traderaroonosc

(PECL trader >= 0.2.0)

traderaroonosc — Осцилятор індикатора Aroon

### Опис

```methodsynopsis
trader_aroonosc(array $high, array $low, int $timePeriod = ?): array
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