---
navigation:
  - function.fann-set-callback.md: « fann\_set\_callback
  - function.fann-set-cascade-activation-steepnesses.md: fann\_set\_cascade\_activation\_steepnesses »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_cascade\_activation\_functions
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_cascade\_activation\_functions

(PECL fann >= 1.0.0)

fann\_set\_cascade\_activation\_functions - Встановлює масив каскадних функцій активації кандидатів

### Опис

```methodsynopsis
fann_set_cascade_activation_functions(resource $ann, array $cascade_activation_functions): bool
```

Встановлює масив каскадних функцій активації кандидатів.

Смотрите[fann\_get\_cascade\_num\_candidates()](function.fann-get-cascade-num-candidates.md) для опису того, які нейрони-кандидати будуть згенеровані цим масивом.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_activation_functions`

Масив каскадних функцій активації кандидатів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_cascade\_activation\_functions\_count()](function.fann-get-cascade-activation-functions-count.md) \- Повертає кількість функцій каскадної активації
-   **fann\_set\_cascade\_activation\_functions()**
