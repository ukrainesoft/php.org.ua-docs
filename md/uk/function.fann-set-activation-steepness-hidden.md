---
navigation:
  - function.fann-set-activation-function.md: « fann\_set\_activation\_function
  - function.fann-set-activation-steepness-layer.md: fann\_set\_activation\_steepness\_layer »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_activation\_steepness\_hidden
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_activation\_steepness\_hidden

(PECL fann >= 1.0.0)

fann\_set\_activation\_steepness\_hidden - Встановлює крутизну крутизни активації для всіх нейронів у всіх прихованих шарах

### Опис

```methodsynopsis
fann_set_activation_steepness_hidden(resource $ann, float $activation_steepness): bool
```

Встановлює крутість крутості активації для всіх нейронів у всіх прихованих шарах.

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
-   [fann\_set\_activation\_steepness\_output()](function.fann-set-activation-steepness-output.md) \- Встановлює крутість активації у вихідному шарі
-   [fann\_get\_activation\_steepness()](function.fann-get-activation-steepness.md) \- Повертає крутість активації для нейрона, що поставляється, і номери шару
-   [fann\_set\_activation\_function()](function.fann-set-activation-function.md) \- Встановлює функцію активації для зазначеного нейрона та шару
