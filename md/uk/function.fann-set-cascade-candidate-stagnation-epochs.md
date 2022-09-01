---
navigation:
  - function.fann-set-cascade-candidate-limit.html: « fannsetcascadecandidatelimit
  - function.fann-set-cascade-max-cand-epochs.html: fannsetcascademaxcandepochs »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetcascadecandidatestagnationepochs
---
# fannsetcascadecandidatestagnationepochs

(PECL fann> = 1.0.0)

fannsetcascadecandidatestagnationepochs - Встановлює кількість каскадних періодів застою кандидатів

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

-   [fanngetcascadecandidatestagnationepochs()](function.fann-get-cascade-candidate-stagnation-epochs.md) - Повертає кількість періодів застою каскаду кандидата
