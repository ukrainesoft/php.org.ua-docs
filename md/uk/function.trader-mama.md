---
navigation:
  - function.trader-macdfix.md: « trader\_macdfix
  - function.trader-mavp.md: trader\_mavp »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_mama
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_mama

(PECL trader >= 0.2.0)

trader\_mama — MESA Адаптивна ковзна середня

### Опис

```methodsynopsis
trader_mama(array $real, float $fastLimit = ?, float $slowLimit = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`fastLimit`

Верхня межа, яка використовується в адаптивному алгоритмі. Допустимі значення від 0.01 до 0.99.

`slowLimit`

Нижня межа, яка використовується в адаптивному алгоритмі. Допустимі значення від 0.01 до 0.99.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
