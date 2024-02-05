---
navigation:
  - function.stats-stat-powersum.md: « stats\_stat\_powersum
  - book.trader.md: Trader »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_variance
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_variance

(PECL stats >= 1.0.0)

stats\_variance - Повертає дисперсію

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

Повертає дисперсію у разі успішного виконання; \*\*`false`\*\*в случае возникновения ошибки.
