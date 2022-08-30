Повертає стандартне відхилення

-   [« statsskew](function.stats-skew.html)
    
-   [statsstatbinomialcoef »](function.stats-stat-binomial-coef.html)
    
-   [PHP Manual](index.html)
    
-   [Функції статистики](ref.stats.html)
    
-   Повертає стандартне відхилення
    

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