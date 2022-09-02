---
navigation:
  - function.fann-set-activation-steepness-layer.md: « fannsetactivationsteepnesslayer
  - function.fann-set-activation-steepness.md: fannsetactivationsteepness »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetactivationsteepnessoutput
---
# fannsetactivationsteepnessoutput

(PECL fann> = 1.0.0)

fannsetactivationsteepnessoutput — Встановлює крутість активації у вихідному шарі

### Опис

```methodsynopsis
fann_set_activation_steepness_output(resource $ann, float $activation_steepness): bool
```

Встановлює крутість активації у вихідному шарі.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`activation_steepness`

Крутизна активації.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fannsetactivationsteepness()](function.fann-set-activation-steepness.md) - Встановлює крутість активації для вказаного нейрона та номера шару
-   [fannsetactivationsteepnesslayer()](function.fann-set-activation-steepness-layer.md) - Встановлює крутість активації для всіх нейронів у вказаному номері шару
-   [fannsetactivationsteepnesshidden()](function.fann-set-activation-steepness-hidden.md) - Встановлює крутість крутості активації для всіх нейронів у всіх прихованих шарах
-   [fanngetactivationsteepness()](function.fann-get-activation-steepness.md) - Повертає крутість активації для нейрона, що поставляється, і номери шару
-   [fannsetactivationfunction()](function.fann-set-activation-function.md) - Встановлює функцію активації для зазначеного нейрона та шару
