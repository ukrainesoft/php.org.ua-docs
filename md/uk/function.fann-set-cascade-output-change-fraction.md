---
navigation:
  - function.fann-set-cascade-num-candidate-groups.html: « fannsetcascadenumcandidategroups
  - function.fann-set-cascade-output-stagnation-epochs.html: fannsetcascadeoutputstagnationepochs »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fannsetcascadeoutputchangefraction
---
# fannsetcascadeoutputchangefraction

(PECL fann> = 1.0.0)

fannsetcascadeoutputchangefraction - Встановлює частку зміни каскадних вихідних даних

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

-   [fanngetcascadeoutputchangefraction()](function.fann-get-cascade-output-change-fraction.html) - Повертає частку зміни виходу каскаду
