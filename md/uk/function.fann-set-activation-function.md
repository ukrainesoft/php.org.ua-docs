---
navigation:
  - function.fann-set-activation-function-output.md: « fann\_set\_activation\_function\_output
  - function.fann-set-activation-steepness-hidden.md: fann\_set\_activation\_steepness\_hidden »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_activation\_function
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_activation\_function

(PECL fann >= 1.0.0)

fann\_set\_activation\_function — Встановлює функцію активації для вказаного нейрона та шару

### Опис

```methodsynopsis
fann_set_activation_function(    resource $ann,    int $activation_function,    int $layer,    int $neuron): bool
```

Установите функцию активации для нейрона номер`neuron` у шарі номер `layer`, Вважаючи вхідний шар як шар 0.

Неможливо встановити функції активації для нейронів у вхідному шарі.

При виборі функції активації важливо враховувати, що функції активації мають різний діапазон . **`FANN_SIGMOID`**, наПриклад, в диапазоне от 0 до 1, в то время как\*\*`FANN_SIGMOID_SYMMETRIC`**находится в диапазоне от -1 до 1, а**`FANN_LINEAR`\*\* без обмежень.

Надане значення activation\_function має бути однією з констант [функцій активації](fann.constants.md#constants.fann-activation-funcs)

Возвращаемое значение - одна из констант[функцій активації](fann.constants.md#constants.fann-train)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`activation_function`

Константа[функцій активації](fann.constants.md#constants.fann-activation-funcs)

`layer`

Номер шару.

`neuron`

Номер нейрона.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_set\_activation\_function\_layer()](function.fann-set-activation-function-layer.md) \- Встановлює функцію активації для всіх нейронів у наданому шарі
-   [fann\_set\_activation\_function\_hidden()](function.fann-set-activation-function-hidden.md) \- Встановлює функцію активації для всіх прихованих шарів
-   [fann\_set\_activation\_function\_output()](function.fann-set-activation-function-output.md) \- Встановлює функцію активації для вихідного шару
-   [fann\_set\_activation\_steepness()](function.fann-set-activation-steepness.md) \- Встановлює крутість активації для вказаного нейрона та номера шару
-   [fann\_get\_activation\_function()](function.fann-get-activation-function.md) \- Повертає функцію активації
