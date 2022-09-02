---
navigation:
  - function.fann-set-cascade-candidate-change-fraction.md: « fannsetcascadecandidatechangefraction
  - function.fann-set-cascade-candidate-stagnation-epochs.md: fannsetcascadecandidatestagnationepochs »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetcascadecandidatelimit
---
# fannsetcascadecandidatelimit

(PECL fann> = 1.0.0)

fannsetcascadecandidatelimit - Встановлює ліміт кандидатів

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

-   [fanngetcascadecandidatelimit()](function.fann-get-cascade-candidate-limit.md) - Повертає межу кандидата
