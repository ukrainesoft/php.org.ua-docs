---
navigation:
  - function.fann-set-activation-steepness-hidden.html: « fannsetactivationsteepnesshidden
  - function.fann-set-activation-steepness-output.html: fannsetactivationsteepnessoutput »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetactivationsteepnesslayer
---
# fannsetactivationsteepnesslayer

(PECL fann> = 1.0.0)

fannsetactivationsteepnesslayer — Встановлює крутизну активації для всіх нейронів у вказаному номері шару

### Опис

```methodsynopsis
fann_set_activation_steepness_layer(resource $ann, float $activation_steepness, int $layer): bool
```

Встановіть крутість активації для всіх нейронів у шарі номер `layer`, Вважаючи вхідний шар як шар 0.

Неможливо встановити крутість активації нейронів у вхідному шарі.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`activation_steepness`

Крутизна активації.

`layer`

Номер шару.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fannsetactivationsteepness()](function.fann-set-activation-steepness.md) - Встановлює крутість активації для вказаного нейрона та номера шару
-   [fannsetactivationsteepnesshidden()](function.fann-set-activation-steepness-hidden.md) - Встановлює крутість крутості активації для всіх нейронів у всіх прихованих шарах
-   [fannsetactivationsteepnessoutput()](function.fann-set-activation-steepness-output.md) - Встановлює крутість активації у вихідному шарі
-   [fanngetactivationsteepness()](function.fann-get-activation-steepness.md) - Повертає крутість активації для нейрона, що поставляється, і номери шару
-   [fannsetactivationfunction()](function.fann-set-activation-function.md) - Встановлює функцію активації для зазначеного нейрона та шару
