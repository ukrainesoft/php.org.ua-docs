- [ trader_ppo](function.trader-ppo.md)
- [trader_rocp »](function.trader-rocp.md)

- [PHP Manual](index.md)
- [Функції Trader](ref.trader.md)
- Швидкість зміни: ((ціна/попередня ціна)-1)\*100

# trader_roc

(PECL trader \>= 0.2.0)

trader_roc — Швидкість зміни: ((ціна/попередня ціна)-1)\*100

### Опис

**trader_roc**(array `$real`, int `$timePeriod` = ?): array

### Список параметрів

`real`
Масив, який містить реальні значення.

`timePeriod`
Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі
виникнення помилки.
