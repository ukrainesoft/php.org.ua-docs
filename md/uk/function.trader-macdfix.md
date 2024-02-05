---
navigation:
  - function.trader-macdext.md: « trader\_macdext
  - function.trader-mama.md: trader\_mama »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_macdfix
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_macdfix

(PECL trader >= 0.2.0)

trader\_macdfix — Виправлення сходження/розходження ковзної середньої 12/26

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
