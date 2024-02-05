---
navigation:
  - function.fann-set-cascade-output-stagnation-epochs.md: « fann\_set\_cascade\_output\_stagnation\_epochs
  - function.fann-set-error-log.md: fann\_set\_error\_log »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_cascade\_weight\_multiplier
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_cascade\_weight\_multiplier

(PECL fann >= 1.0.0)

fann\_set\_cascade\_weight\_multiplier - Встановлює множник ваги

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

-   [fann\_get\_cascade\_weight\_multiplier()](function.fann-get-cascade-weight-multiplier.md) \- Повертає множник ваги
