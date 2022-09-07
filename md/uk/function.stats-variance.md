---
navigation:
  - function.stats-stat-powersum.md: « statsstatpowersum
  - book.trader.md: Trader »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: statsvariance
---
# statsvariance

(PECL stats >= 1.0.0)

statsvariance - Повертає дисперсію

### Опис

```methodsynopsis
stats_variance(array $a, bool $sample = false): float
```

Повертає дисперсію значень у `a`

### Список параметрів

`a`

Масив даних, для якого потрібно знайти стандартне відхилення. Зверніть увагу, що всі значення масиву будуть перетворені на число з плаваючою точкою (float).

`sample`

Вказує, чи представляє `a` вибірку населення; за замовчуванням **`false`**

### Значення, що повертаються

Повертає дисперсію у разі успішного виконання; **`false`** у разі виникнення помилки.
