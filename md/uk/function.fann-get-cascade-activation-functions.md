---
navigation:
  - function.fann-get-cascade-activation-functions-count.md: « fann\_get\_cascade\_activation\_functions\_count
  - function.fann-get-cascade-activation-steepnesses-count.md: fann\_get\_cascade\_activation\_steepnesses\_count »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_cascade\_activation\_functions
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_cascade\_activation\_functions

(PECL fann >= 1.0.0)

fann\_get\_cascade\_activation\_functions — Повертає функції каскадної активації

### Опис

```methodsynopsis
fann_get_cascade_activation_functions(resource $ann): array
```

Масив функцій каскадної активації – це масив різних функцій активації, які використовуються кандидатами.

Смотрите[fann\_get\_cascade\_num\_candidates()](function.fann-get-cascade-num-candidates.md) для опису того, які нейрони кандидата генеруватимуться цим масивом.

Функції активації за замовчуванням: **`FANN_SIGMOID`** **`FANN_SIGMOID_SYMMETRIC`** **`FANN_GAUSSIAN`** **`FANN_GAUSSIAN_SYMMETRIC`** **`FANN_ELLIOT`** **`FANN_ELLIOT_SYMMETRIC`**

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Функції каскадної активації або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_get\_cascade\_activation\_functions\_count()](function.fann-get-cascade-activation-functions-count.md) \- Повертає кількість функцій каскадної активації
-   [fann\_set\_cascade\_activation\_functions()](function.fann-set-cascade-activation-functions.md) \- встановлює масив каскадних функцій активації кандидатів
