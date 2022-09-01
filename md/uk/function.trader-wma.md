---
navigation:
  - function.trader-willr.html: « traderwillr
  - refs.utilspec.nontext.md: Генерація нетекстових MIME-форматів
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderwma
---
# traderwma

(PECL trader >= 0.2.0)

traderwma — Зважена ковзна середня

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
