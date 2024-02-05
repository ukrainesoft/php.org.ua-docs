---
navigation:
  - function.fann-set-activation-steepness-output.md: « fann\_set\_activation\_steepness\_output
  - function.fann-set-bit-fail-limit.md: fann\_set\_bit\_fail\_limit »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_activation\_steepness
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_activation\_steepness

(PECL fann >= 1.0.0)

fann\_set\_activation\_steepness — Встановлює крутизну активації для вказаного нейрона та номера шару

### Опис

```methodsynopsis
fann_set_activation_steepness(    resource $ann,    float $activation_steepness,    int $layer,    int $neuron): bool
```

Установите крутизну активации для нейрона номер`neuron` у шарі номер `layer`, Вважаючи вхідний шар як шар 0.

Неможливо встановити крутість активації нейронів у вхідному шарі.

Крутизна функції активації дещо свідчить, наскільки швидко функція активації переходить від мінімуму до максимуму. Високе значення функції активації також надасть більш агресивне навчання.

Під час навчання нейронних мереж, у яких вихідні значення мають бути крайніми (зазвичай 0 і 1, залежно від функції активації), можна використовувати крута функція активації (наприклад, 1.0).

За умовчанням крутість активації становить 0.5.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`activation_steepness`

Крутизна активації.

`layer`

Номер шару.

`neuron`

Номер нейрона.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_set\_activation\_steepness\_layer()](function.fann-set-activation-steepness-layer.md) \- Встановлює крутість активації для всіх нейронів у вказаному номері шару
-   [fann\_set\_activation\_steepness\_hidden()](function.fann-set-activation-steepness-hidden.md) \- Встановлює крутість крутості активації для всіх нейронів у всіх прихованих шарах
-   [fann\_set\_activation\_steepness\_output()](function.fann-set-activation-steepness-output.md) \- Встановлює крутість активації у вихідному шарі
-   [fann\_get\_activation\_steepness()](function.fann-get-activation-steepness.md) \- Повертає крутість активації для нейрона, що поставляється, і номери шару
-   [fann\_set\_activation\_function()](function.fann-set-activation-function.md) \- Встановлює функцію активації для зазначеного нейрона та шару
