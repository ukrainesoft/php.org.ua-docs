---
navigation:
  - function.trader-macdext.md: « tradermacdext
  - function.trader-mama.md: tradermama »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradermacdfix
---
# tradermacdfix

(PECL trader >= 0.2.0)

tradermacdfix — Виправлення сходження/розходження ковзної середньої 12/26

### Опис

```methodsynopsis
trader_macdfix(array $real, int $signalPeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`signalPeriod`

Згладжування сигнальної лінії (номер періоду). Допустимі значення від 1 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
