---
navigation:
  - function.stats-skew.md: « statsskew
  - function.stats-stat-binomial-coef.md: statsstatbinomialcoef »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: statsstandarddeviation
---
# statsstandarddeviation

(PECL stats >= 1.0.0)

statsstandarddeviation — Повертає стандартне відхилення

### Опис

```methodsynopsis
stats_standard_deviation(array $a, bool $sample = false): float
```

Повертає стандартне відхилення для масиву значень `a`

### Список параметрів

`a`

Масив із даними для пошуку стандартного відхилення. Зверніть увагу, що всі значення масиву будуть приведені до типу float.

`sample`

Вказує, що параметр `a` є вибіркою з генеральної сукупності. За замовчуванням **`false`**

### Значення, що повертаються

Повертає стандартне відхилення у разі успішного виконання; **`false`** у разі виникнення помилки.

### Помилки

Викликає попередження **`E_WARNING`**, якщо у параметрі `a` менше двох значень.
