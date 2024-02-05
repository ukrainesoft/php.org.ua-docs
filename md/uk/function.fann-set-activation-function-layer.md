---
navigation:
  - function.fann-set-activation-function-hidden.md: « fann\_set\_activation\_function\_hidden
  - function.fann-set-activation-function-output.md: fann\_set\_activation\_function\_output »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_activation\_function\_layer
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_activation\_function\_layer

(PECL fann >= 1.0.0)

fann\_set\_activation\_function\_layer — Встановлює функцію активації для всіх нейронів у наданому шарі

### Опис

```methodsynopsis
fann_set_activation_function_layer(resource $ann, int $activation_function, int $layer): bool
```

Встановіть функцію активації всіх нейронів у шарі номер `layer`, Вважаючи вхідний шар шаром 0.

Неможливо встановити функції активації для нейронів у вхідному шарі.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`activation_function`

Константа[функцій активації](fann.constants.md#constants.fann-activation-funcs)

`layer`

Номер шару.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_set\_activation\_function()](function.fann-set-activation-function.md) \- Встановлює функцію активації для зазначеного нейрона та шару
-   [fann\_set\_activation\_function\_hidden()](function.fann-set-activation-function-hidden.md) \- Встановлює функцію активації для всіх прихованих шарів
-   [fann\_set\_activation\_function\_output()](function.fann-set-activation-function-output.md) \- Встановлює функцію активації для вихідного шару
-   [fann\_set\_activation\_steepness()](function.fann-set-activation-steepness.md) \- Встановлює крутість активації для вказаного нейрона та номера шару
