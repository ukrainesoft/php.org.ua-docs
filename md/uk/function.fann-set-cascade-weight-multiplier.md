---
navigation:
  - function.fann-set-cascade-output-stagnation-epochs.html: « fannsetcascadeoutputstagnationepochs
  - function.fann-set-error-log.html: fannseterrorlog »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fannsetcascadeweightmultiplier
---
# fannsetcascadeweightmultiplier

(PECL fann> = 1.0.0)

fannsetcascadeweightmultiplier - Встановлює множник ваги

### Опис

```methodsynopsis
fann_set_cascade_weight_multiplier(resource $ann, float $cascade_weight_multiplier): bool
```

Встановлює множник ваги.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_weight_multiplier`

Множина ваги.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngetcascadeweightmultiplier()](function.fann-get-cascade-weight-multiplier.html) - Повертає множник ваги
