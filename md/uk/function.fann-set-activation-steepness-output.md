---
navigation:
  - function.fann-set-activation-steepness-layer.md: « fann\_set\_activation\_steepness\_layer
  - function.fann-set-activation-steepness.md: fann\_set\_activation\_steepness »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_activation\_steepness\_output
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_activation\_steepness\_output

(PECL fann >= 1.0.0)

fann\_set\_activation\_steepness\_output — Встановлює крутість активації у вихідному шарі

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

-   [fann\_set\_activation\_steepness()](function.fann-set-activation-steepness.md) \- Встановлює крутість активації для вказаного нейрона та номера шару
-   [fann\_set\_activation\_steepness\_layer()](function.fann-set-activation-steepness-layer.md) \- Встановлює крутість активації для всіх нейронів у вказаному номері шару
-   [fann\_set\_activation\_steepness\_hidden()](function.fann-set-activation-steepness-hidden.md) \- Встановлює крутість крутості активації для всіх нейронів у всіх прихованих шарах
-   [fann\_get\_activation\_steepness()](function.fann-get-activation-steepness.md) \- Повертає крутість активації для нейрона, що поставляється, і номери шару
-   [fann\_set\_activation\_function()](function.fann-set-activation-function.md) \- Встановлює функцію активації для зазначеного нейрона та шару
