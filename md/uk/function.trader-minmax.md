- [«trader_minindex](function.trader-minindex.md)
- [trader_minmaxindex »](function.trader-minmaxindex.md)

- [PHP Manual](index.md)
- [Функції Trader](ref.trader.md)
- Найнижчі та найвищі значення за вказаний період

#trader_minmax

(PECL trader \>= 0.2.0)

trader_minmax — Найнижчі та найвищі значення за вказаний
період

### Опис

**trader_minmax**(array `$real`, int `$timePeriod` = ?): array

### Список параметрів

`real`
Масив, який містить реальні значення.

`timePeriod`
Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі
виникнення помилки.
