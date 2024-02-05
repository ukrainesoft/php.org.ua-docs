---
navigation:
  - function.fann-set-cascade-max-cand-epochs.md: « fann\_set\_cascade\_max\_cand\_epochs
  - function.fann-set-cascade-min-cand-epochs.md: fann\_set\_cascade\_min\_cand\_epochs »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_cascade\_max\_out\_epochs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_cascade\_max\_out\_epochs

(PECL fann >= 1.0.0)

fann\_set\_cascade\_max\_out\_epochs - Встановлює максимальну кількість епох

### Опис

```methodsynopsis
fann_set_cascade_max_out_epochs(resource $ann, int $cascade_max_out_epochs): bool
```

Встановлює максимальну кількість епох.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_max_out_epochs`

Максимальна кількість епох.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_cascade\_max\_out\_epochs()](function.fann-get-cascade-max-out-epochs.md) \- Повертає максимальну кількість періодів
