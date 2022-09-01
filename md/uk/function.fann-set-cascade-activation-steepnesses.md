---
navigation:
  - function.fann-set-cascade-activation-functions.html: « fannsetcascadeactivationfunctions
  - function.fann-set-cascade-candidate-change-fraction.html: fannsetcascadecandidatechangefraction »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fannsetcascadeactivationsteepnesses
---
# fannsetcascadeactivationsteepnesses

(PECL fann> = 1.0.0)

fannsetcascadeactivationsteepnesses - Встановлює масив крутості включення кандидатів у каскад

### Опис

```methodsynopsis
fann_set_cascade_activation_steepnesses(resource $ann, array $cascade_activation_steepnesses_count): bool
```

Встановлює масив крутості включення кандидатів у каскад.

Дивіться [fanngetcascadenumcandidates()](function.fann-get-cascade-num-candidates.html) для опису того, які нейрони-кандидати будуть згенеровані цим масивом.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_activation_steepnesses_count`

Масив крутості включення кандидатів у каскад.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngetcascadeactivationsteepnesses()](function.fann-get-cascade-activation-steepnesses.html) - Повертає крутість каскадної активації
-   [fanngetcascadeactivationsteepnessescount()](function.fann-get-cascade-activation-steepnesses-count.html) - Кількість крутості активації
