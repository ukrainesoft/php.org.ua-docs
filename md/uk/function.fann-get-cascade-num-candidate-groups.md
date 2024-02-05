---
navigation:
  - function.fann-get-cascade-min-out-epochs.md: « fann\_get\_cascade\_min\_out\_epochs
  - function.fann-get-cascade-num-candidates.md: fann\_get\_cascade\_num\_candidates »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_cascade\_num\_candidate\_groups
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_cascade\_num\_candidate\_groups

(PECL fann >= 1.0.0)

fann\_get\_cascade\_num\_candidate\_groups — Повертає кількість груп кандидатів

### Опис

```methodsynopsis
fann_get_cascade_num_candidate_groups(resource $ann): int
```

Кількість груп кандидатів – це кількість груп однакових кандидатів, які використовуватимуться під час навчання.

Кількість можна використовувати, щоб збільшити кількість кандидатів без необхідності визначати нові параметри для кандидатів.

Смотрите[fann\_get\_cascade\_num\_candidates()](function.fann-get-cascade-num-candidates.md) для опису того, які нейрони-кандидати будуть згенеровані цим параметром.

Кількість груп кандидатів за умовчанням дорівнює 2.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Кількість груп кандидатів або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_cascade\_num\_candidate\_groups()](function.fann-set-cascade-num-candidate-groups.md) \- встановлює кількість груп кандидатів
