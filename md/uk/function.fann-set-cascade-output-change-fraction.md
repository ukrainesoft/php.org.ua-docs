---
navigation:
  - function.fann-set-cascade-num-candidate-groups.md: « fann\_set\_cascade\_num\_candidate\_groups
  - function.fann-set-cascade-output-stagnation-epochs.md: fann\_set\_cascade\_output\_stagnation\_epochs »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_cascade\_output\_change\_fraction
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_cascade\_output\_change\_fraction

(PECL fann >= 1.0.0)

fann\_set\_cascade\_output\_change\_fraction - Встановлює частку зміни каскадних вихідних даних

### Опис

```methodsynopsis
fann_set_cascade_output_change_fraction(resource $ann, float $cascade_output_change_fraction): bool
```

Встановлює частку зміни каскадних вихідних даних.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_output_change_fraction`

Частка змін каскадних вихідних даних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_cascade\_output\_change\_fraction()](function.fann-get-cascade-output-change-fraction.md) \- Повертає частку зміни виходу каскаду
