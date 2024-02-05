---
navigation:
  - function.fann-set-cascade-candidate-change-fraction.md: « fann\_set\_cascade\_candidate\_change\_fraction
  - function.fann-set-cascade-candidate-stagnation-epochs.md: fann\_set\_cascade\_candidate\_stagnation\_epochs »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_cascade\_candidate\_limit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_cascade\_candidate\_limit

(PECL fann >= 1.0.0)

fann\_set\_cascade\_candidate\_limit - Встановлює ліміт кандидатів

### Опис

```methodsynopsis
fann_set_cascade_candidate_limit(resource $ann, float $cascade_candidate_limit): bool
```

Встановлює ліміт кандидатів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_candidate_limit`

Ліміт кандидатів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_cascade\_candidate\_limit()](function.fann-get-cascade-candidate-limit.md) \- Повертає межу кандидата
