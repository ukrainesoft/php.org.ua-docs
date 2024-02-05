---
navigation:
  - function.fann-set-cascade-min-out-epochs.md: « fann\_set\_cascade\_min\_out\_epochs
  - function.fann-set-cascade-output-change-fraction.md: fann\_set\_cascade\_output\_change\_fraction »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_cascade\_num\_candidate\_groups
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_cascade\_num\_candidate\_groups

(PECL fann >= 1.0.0)

fann\_set\_cascade\_num\_candidate\_groups - Встановлює кількість груп кандидатів

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

-   [fann\_get\_cascade\_num\_candidate\_groups()](function.fann-get-cascade-num-candidate-groups.md) \- Повертає кількість груп кандидатів
