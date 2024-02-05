---
navigation:
  - function.fann-scale-train.md: « fann\_scale\_train
  - function.fann-set-activation-function-layer.md: fann\_set\_activation\_function\_layer »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_activation\_function\_hidden
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_activation\_function\_hidden

(PECL fann >= 1.0.0)

fann\_set\_activation\_function\_hidden — Встановлює функцію активації для всіх прихованих шарів

### Опис

```methodsynopsis
fann_set_activation_function_hidden(resource $ann, int $activation_function): bool
```

Встановлює функцію активації всіх прихованих шарів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`activation_function`

Константа[функцій активації](fann.constants.md#constants.fann-activation-funcs)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_set\_activation\_function()](function.fann-set-activation-function.md) \- Встановлює функцію активації для зазначеного нейрона та шару
-   [fann\_set\_activation\_function\_layer()](function.fann-set-activation-function-layer.md) \- Встановлює функцію активації для всіх нейронів у наданому шарі
-   [fann\_set\_activation\_function\_output()](function.fann-set-activation-function-output.md) \- Встановлює функцію активації для вихідного шару
-   [fann\_set\_activation\_steepness()](function.fann-set-activation-steepness.md) \- Встановлює крутість активації для вказаного нейрона та номера шару
