---
navigation:
  - function.stats-skew.md: « stats\_skew
  - function.stats-stat-binomial-coef.md: stats\_stat\_binomial\_coef »
  - index.md: PHP Manual
  - ref.stats.md: Функції статистики
title: stats\_standard\_deviation
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stats\_standard\_deviation

(PECL stats >= 1.0.0)

stats\_standard\_deviation — Повертає стандартне відхилення

### Опис

```methodsynopsis
stats_standard_deviation(array $a, bool $sample = false): float
```

Возвращает стандартное отклонение для массива значений`a`

### Список параметрів

`a`

Масив із даними для пошуку стандартного відхилення. Зверніть увагу, що всі значення масиву будуть приведені до типу float.

`sample`

Вказує, що параметр `a` є вибіркою з генеральної сукупності. За замовчуванням **`false`**

### Значення, що повертаються

Повертає стандартне відхилення у разі успішного виконання; \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Викликає попередження **`E_WARNING`**, якщо у параметрі `a`меньше двух значений.
