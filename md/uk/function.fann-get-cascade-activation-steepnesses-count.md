---
navigation:
  - function.fann-get-cascade-activation-functions.html: « fanngetcascadeactivationfunctions
  - function.fann-get-cascade-activation-steepnesses.html: fanngetcascadeactivationsteepnesses »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fanngetcascadeactivationsteepnessescount
---
# fanngetcascadeactivationsteepnessescount

(PECL fann> = 1.0.0)

fanngetcascadeactivationsteepnessescount — Кількість крутості активації

### Опис

```methodsynopsis
fann_get_cascade_activation_steepnesses_count(resource $ann): int
```

Кількість крутості активації в масиві [fanngetcascadeactivationfunctions()](function.fann-get-cascade-activation-functions.html)

Кількість крутизни за замовчуванням активації - 4.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Кількість крутості активації або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fanngetcascadeactivationsteepnesses()](function.fann-get-cascade-activation-steepnesses.html) - Повертає крутість каскадної активації
-   [fannsetcascadeactivationfunctions()](function.fann-set-cascade-activation-functions.html) - встановлює масив каскадних функцій активації кандидатів
