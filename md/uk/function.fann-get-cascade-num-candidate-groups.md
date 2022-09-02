---
navigation:
  - function.fann-get-cascade-min-out-epochs.md: « fanngetcascademinoutepochs
  - function.fann-get-cascade-num-candidates.md: fanngetcascadenumcandidates »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetcascadenumcandidategroups
---
# fanngetcascadenumcandidategroups

(PECL fann> = 1.0.0)

fanngetcascadenumcandidategroups — Повертає кількість груп кандидатів

### Опис

```methodsynopsis
fann_get_cascade_num_candidate_groups(resource $ann): int
```

Кількість груп кандидатів – це кількість груп однакових кандидатів, які використовуватимуться під час навчання.

Кількість можна використовувати, щоб збільшити кількість кандидатів без необхідності визначати нові параметри для кандидатів.

Дивіться [fanngetcascadenumcandidates()](function.fann-get-cascade-num-candidates.md) для опису того, які нейрони-кандидати будуть згенеровані цим параметром.

Кількість груп кандидатів за умовчанням дорівнює 2.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Кількість груп кандидатів або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsetcascadenumcandidategroups()](function.fann-set-cascade-num-candidate-groups.md) - встановлює кількість груп кандидатів
