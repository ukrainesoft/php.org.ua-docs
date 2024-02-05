---
navigation:
  - function.fann-set-cascade-activation-functions.md: « fann\_set\_cascade\_activation\_functions
  - function.fann-set-cascade-candidate-change-fraction.md: fann\_set\_cascade\_candidate\_change\_fraction »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_cascade\_activation\_steepnesses
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_cascade\_activation\_steepnesses

(PECL fann >= 1.0.0)

fann\_set\_cascade\_activation\_steepnesses - Встановлює масив крутості включення кандидатів у каскад

### Опис

```methodsynopsis
fann_set_cascade_activation_steepnesses(resource $ann, array $cascade_activation_steepnesses_count): bool
```

Встановлює масив крутості включення кандидатів у каскад.

Смотрите[fann\_get\_cascade\_num\_candidates()](function.fann-get-cascade-num-candidates.md) для опису того, які нейрони-кандидати будуть згенеровані цим масивом.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_activation_steepnesses_count`

Масив крутості включення кандидатів у каскад.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_cascade\_activation\_steepnesses()](function.fann-get-cascade-activation-steepnesses.md) \- Повертає крутість каскадної активації
-   [fann\_get\_cascade\_activation\_steepnesses\_count()](function.fann-get-cascade-activation-steepnesses-count.md) \- Кількість крутості активації
