---
navigation:
  - function.trader-willr.md: « trader\_willr
  - refs.utilspec.nontext.md: Генерація нетекстових MIME-форматів
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_wma
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_wma

(PECL trader >= 0.2.0)

trader\_wma — Зважена ковзна середня

### Опис

```methodsynopsis
trader_wma(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
