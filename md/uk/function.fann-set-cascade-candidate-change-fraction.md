---
navigation:
  - function.fann-set-cascade-activation-steepnesses.md: « fannsetcascadeactivationsteepnesses
  - function.fann-set-cascade-candidate-limit.md: fannsetcascadecandidatelimit »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetcascadecandidatechangefraction
---
# fannsetcascadecandidatechangefraction

(PECL fann> = 1.0.0)

fannsetcascadecandidatechangefraction - Встановлює частку каскадної зміни кандидата

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

-   [fanngetcascadecandidatechangefraction()](function.fann-get-cascade-candidate-change-fraction.md) - Повертає частку зміни каскаду кандидата
