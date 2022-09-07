---
navigation:
  - function.fann-set-cascade-candidate-stagnation-epochs.md: « fannsetcascadecandidatestagnationepochs
  - function.fann-set-cascade-max-out-epochs.md: fannsetcascademaxoutepochs »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetcascademaxcandepochs
---
# fannsetcascademaxcandepochs

(PECL fann> = 1.0.0)

fannsetcascademaxcandepochs - Встановлює найбільший період кандидата

### Опис

```methodsynopsis
fann_set_cascade_max_cand_epochs(resource $ann, int $cascade_max_cand_epochs): bool
```

Встановлює максимальний період кандидата.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_max_cand_epochs`

Максимальний період кандидата.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngetcascademaxcandepochs()](function.fann-get-cascade-max-cand-epochs.md) - Отримує найбільший період кандидата
