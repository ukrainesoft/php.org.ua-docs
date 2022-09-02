---
navigation:
  - function.fann-duplicate-train-data.md: « fannduplicatetraindata
  - function.fann-get-activation-steepness.md: fanngetactivationsteepness »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetactivationfunction
---
# fanngetactivationfunction

(PECL fann> = 1.0.0)

fanngetactivationfunction — Повертає функцію активації

### Опис

```methodsynopsis
fann_get_activation_function(resource $ann, int $layer, int $neuron): int
```

Отримує функцію активації номера нейрона `neuron` у шарі номер `layer`, Вважаючи вхідний шар як шар 0.

Неможливо отримати функції активації для нейронів у вхідному шарі.

Значення, що повертається, є однією з констант [функцій активації](fann.constants.md#constants.fann-activation-funcs)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`layer`

Номер шару.

`neuron`

Номер нейрона.

### Значення, що повертаються

Константа [функций обучения](fann.constants.md#constants.fann-train) або -1, якщо нейрон не визначений у нейронній мережі або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsetactivationfunctionlayer()](function.fann-set-activation-function-layer.md) - Встановлює функцію активації для всіх нейронів у наданому шарі
-   [fannsetactivationfunctionhidden()](function.fann-set-activation-function-hidden.md) - Встановлює функцію активації для всіх прихованих шарів
-   [fannsetactivationfunctionoutput()](function.fann-set-activation-function-output.md) - Встановлює функцію активації для вихідного шару
-   [fannsetactivationsteepness()](function.fann-set-activation-steepness.md) - Встановлює крутість активації для вказаного нейрона та номера шару
-   [fannsetactivationfunction()](function.fann-set-activation-function.md) - Встановлює функцію активації для зазначеного нейрона та шару
