---
navigation:
  - function.fann-get-bit-fail.html: « fanngetbitfail
  - function.fann-get-cascade-activation-functions.html: fanngetcascadeactivationfunctions »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetcascadeactivationфункційcount
---
# fanngetcascadeactivationфункційcount

(PECL fann> = 1.0.0)

fanngetcascadeactivationфункційcount — Повертає кількість функцій каскадної активації

### Опис

```methodsynopsis
fann_get_cascade_activation_functions_count(resource $ann): int
```

Кількість функцій активації у масиві [fanngetcascadeactivationfunctions()](function.fann-get-cascade-activation-functions.md)

Кількість функцій активації за промовчанням - 6.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Кількість функцій каскадної активації або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fanngetcascadeactivationfunctions()](function.fann-get-cascade-activation-functions.md) - Повертає функції каскадної активації
-   [fannsetcascadeactivationfunctions()](function.fann-set-cascade-activation-functions.md) - встановлює масив каскадних функцій активації кандидатів
