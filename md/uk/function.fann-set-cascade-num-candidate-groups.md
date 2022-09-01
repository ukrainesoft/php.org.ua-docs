---
navigation:
  - function.fann-set-cascade-min-out-epochs.html: « fannsetcascademinoutepochs
  - function.fann-set-cascade-output-change-fraction.html: fannsetcascadeoutputchangefraction »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fannsetcascadenumcandidategroups
---
# fannsetcascadenumcandidategroups

(PECL fann> = 1.0.0)

fannsetcascadenumcandidategroups - Встановлює кількість груп кандидатів

### Опис

```methodsynopsis
fann_set_cascade_num_candidate_groups(resource $ann, int $cascade_num_candidate_groups): bool
```

Встановлює кількість груп кандидатів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_num_candidate_groups`

Кількість груп кандидатів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngetcascadenumcandidategroups()](function.fann-get-cascade-num-candidate-groups.html) - Повертає кількість груп кандидатів
