---
navigation:
  - function.fann-set-cascade-min-cand-epochs.md: « fann\_set\_cascade\_min\_cand\_epochs
  - function.fann-set-cascade-num-candidate-groups.md: fann\_set\_cascade\_num\_candidate\_groups »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_cascade\_min\_out\_epochs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_cascade\_min\_out\_epochs

(PECL fann >= 1.0.0)

fann\_set\_cascade\_min\_out\_epochs - Встановлює мінімальні епохи вихідних даних

### Опис

```methodsynopsis
fann_set_cascade_min_out_epochs(resource $ann, int $cascade_min_out_epochs): bool
```

Встановлює мінімальні доби вихідних даних.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_min_out_epochs`

Мінімальні епохи вихідних даних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Примітки

> **Зауваження** :
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_get\_cascade\_min\_out\_epochs()](function.fann-get-cascade-min-out-epochs.md) \- Повертає мінімальну кількість періодів
