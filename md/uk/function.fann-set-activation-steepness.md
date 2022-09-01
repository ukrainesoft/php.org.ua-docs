---
navigation:
  - function.fann-set-activation-steepness-output.html: « fannsetactivationsteepnessoutput
  - function.fann-set-bit-fail-limit.html: fannsetbitfaillimit »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetactivationsteepness
---
# fannsetactivationsteepness

(PECL fann> = 1.0.0)

fannsetactivationsteepness — Встановлює крутизну активації для вказаного нейрона та номера шару

### Опис

```methodsynopsis
fann_set_activation_steepness(    resource $ann,    float $activation_steepness,    int $layer,    int $neuron): bool
```

Встановіть крутість активації для нейрона номер `neuron` у шарі номер `layer`, Вважаючи вхідний шар як шар 0.

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

-   [fannsetactivationsteepnesslayer()](function.fann-set-activation-steepness-layer.md) - Встановлює крутість активації для всіх нейронів у вказаному номері шару
-   [fannsetactivationsteepnesshidden()](function.fann-set-activation-steepness-hidden.md) - Встановлює крутість крутості активації для всіх нейронів у всіх прихованих шарах
-   [fannsetactivationsteepnessoutput()](function.fann-set-activation-steepness-output.md) - Встановлює крутість активації у вихідному шарі
-   [fanngetactivationsteepness()](function.fann-get-activation-steepness.md) - Повертає крутість активації для нейрона, що поставляється, і номери шару
-   [fannsetactivationfunction()](function.fann-set-activation-function.md) - Встановлює функцію активації для зазначеного нейрона та шару
