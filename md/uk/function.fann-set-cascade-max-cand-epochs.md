---
navigation:
  - function.fann-set-cascade-candidate-stagnation-epochs.md: « fann\_set\_cascade\_candidate\_stagnation\_epochs
  - function.fann-set-cascade-max-out-epochs.md: fann\_set\_cascade\_max\_out\_epochs »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_cascade\_max\_cand\_epochs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_cascade\_max\_cand\_epochs

(PECL fann >= 1.0.0)

fann\_set\_cascade\_max\_cand\_epochs - Встановлює найбільший період кандидата

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

-   [fann\_get\_cascade\_max\_cand\_epochs()](function.fann-get-cascade-max-cand-epochs.md) \- Отримує найбільший період кандидата
