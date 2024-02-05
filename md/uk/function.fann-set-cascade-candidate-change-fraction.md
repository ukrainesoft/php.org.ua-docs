---
navigation:
  - function.fann-set-cascade-activation-steepnesses.md: « fann\_set\_cascade\_activation\_steepnesses
  - function.fann-set-cascade-candidate-limit.md: fann\_set\_cascade\_candidate\_limit »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_cascade\_candidate\_change\_fraction
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_cascade\_candidate\_change\_fraction

(PECL fann >= 1.0.0)

fann\_set\_cascade\_candidate\_change\_fraction - Встановлює частку каскадної зміни кандидата

### Опис

```methodsynopsis
fann_set_cascade_candidate_change_fraction(resource $ann, float $cascade_candidate_change_fraction): bool
```

Встановлює частку каскадної зміни кандидата.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_candidate_change_fraction`

Частка каскадної зміни кандидата.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_cascade\_candidate\_change\_fraction()](function.fann-get-cascade-candidate-change-fraction.md) \- Повертає частку зміни каскаду кандидата
