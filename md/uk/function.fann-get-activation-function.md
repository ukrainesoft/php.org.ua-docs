---
navigation:
  - function.fann-duplicate-train-data.md: « fann\_duplicate\_train\_data
  - function.fann-get-activation-steepness.md: fann\_get\_activation\_steepness »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_activation\_function
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_activation\_function

(PECL fann >= 1.0.0)

fann\_get\_activation\_function — Повертає функцію активації

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

Константа[функцій навчання](fann.constants.md#constants.fann-train) або -1, якщо нейрон не визначений у нейронній мережі або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_activation\_function\_layer()](function.fann-set-activation-function-layer.md) \- Встановлює функцію активації для всіх нейронів у наданому шарі
-   [fann\_set\_activation\_function\_hidden()](function.fann-set-activation-function-hidden.md) \- Встановлює функцію активації для всіх прихованих шарів
-   [fann\_set\_activation\_function\_output()](function.fann-set-activation-function-output.md) \- Встановлює функцію активації для вихідного шару
-   [fann\_set\_activation\_steepness()](function.fann-set-activation-steepness.md) \- Встановлює крутість активації для вказаного нейрона та номера шару
-   [fann\_set\_activation\_function()](function.fann-set-activation-function.md) \- Встановлює функцію активації для зазначеного нейрона та шару
