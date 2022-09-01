---
navigation:
  - function.fann-get-cascade-activation-steepnesses-count.html: « fanngetcascadeactivationsteepnessescount
  - function.fann-get-cascade-candidate-change-fraction.html: fanngetcascadecandidatechangefraction »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fanngetcascadeactivationsteepnesses
---
# fanngetcascadeactivationsteepnesses

(PECL fann> = 1.0.0)

fanngetcascadeactivationsteepnesses — Повертає крутість каскадної активації

### Опис

```methodsynopsis
fann_get_cascade_activation_steepnesses(resource $ann): array
```

Масив крутості каскадної активації – це масив різних функцій активації, які використовуються кандидатами.

Дивіться [fanngetcascadenumcandidates()](function.fann-get-cascade-num-candidates.html) для опису того, які кандидатні нейрони генеруватимуться цим масивом.

Крутизна активації за промовчанням: {0,25, 0,50, 0,75, 1,00}.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Крутизна каскадної активації або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fanngetcascadeactivationsteepnessescount()](function.fann-get-cascade-activation-steepnesses-count.html) - Кількість крутості активації
-   [fannsetcascadeactivationsteepnesses()](function.fann-set-cascade-activation-steepnesses.html) - Встановлює масив крутості включення кандидатів у каскад
