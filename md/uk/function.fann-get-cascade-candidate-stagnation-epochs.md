---
navigation:
  - function.fann-get-cascade-candidate-limit.md: « fanngetcascadecandidatelimit
  - function.fann-get-cascade-max-cand-epochs.md: fanngetcascademaxcandepochs »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetcascadecandidatestagnationepochs
---
# fanngetcascadecandidatestagnationepochs

(PECL fann> = 1.0.0)

fanngetcascadecandidatestagnationepochs - Повертає кількість періодів застою каскаду кандидата

### Опис

```methodsynopsis
fann_get_cascade_candidate_stagnation_epochs(resource $ann): int
```

Кількість періодів застою каскаду кандидата визначає кількість періодів, яким дозволено продовжити навчання без зміни MSE на частку [fanngetcascadecandidatechangefraction()](function.fann-get-cascade-candidate-change-fraction.md)

Дивіться додаткову інформацію про цей параметр у [fanngetcascadecandidatechangefraction()](function.fann-get-cascade-candidate-change-fraction.md)

За замовчуванням кількість періодів застою каскаду кандидата дорівнює 12.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Кількість періодів застою каскаду кандидата або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsetcascadecandidatestagnationepochs()](function.fann-set-cascade-candidate-stagnation-epochs.md) - встановлює кількість каскадних періодів застою кандидатів
-   [fanngetcascadecandidatechangefraction()](function.fann-get-cascade-candidate-change-fraction.md) - Повертає частку зміни каскаду кандидата
