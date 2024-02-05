---
navigation:
  - function.fann-set-cascade-candidate-limit.md: « fann\_set\_cascade\_candidate\_limit
  - function.fann-set-cascade-max-cand-epochs.md: fann\_set\_cascade\_max\_cand\_epochs »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_cascade\_candidate\_stagnation\_epochs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_cascade\_candidate\_stagnation\_epochs

(PECL fann >= 1.0.0)

fann\_set\_cascade\_candidate\_stagnation\_epochs - Встановлює кількість каскадних періодів застою кандидатів

### Опис

```methodsynopsis
fann_set_cascade_candidate_stagnation_epochs(resource $ann, int $cascade_candidate_stagnation_epochs): bool
```

Встановлює кількість каскадних періодів застою кандидатів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_candidate_stagnation_epochs`

Кількість каскадних періодів застою кандидатів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_cascade\_candidate\_stagnation\_epochs()](function.fann-get-cascade-candidate-stagnation-epochs.md) \- Повертає кількість періодів застою каскаду кандидата
