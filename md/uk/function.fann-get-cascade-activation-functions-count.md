---
navigation:
  - function.fann-get-bit-fail.md: « fann\_get\_bit\_fail
  - function.fann-get-cascade-activation-functions.md: fann\_get\_cascade\_activation\_functions »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_cascade\_activation\_functions\_count
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_cascade\_activation\_functions\_count

(PECL fann >= 1.0.0)

fann\_get\_cascade\_activation\_functions\_count — Повертає кількість функцій каскадної активації

### Опис

```methodsynopsis
fann_get_cascade_activation_functions_count(resource $ann): int
```

Кількість функцій активації у масиві [fann\_get\_cascade\_activation\_functions()](function.fann-get-cascade-activation-functions.md)

Кількість функцій активації за промовчанням - 6.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Кількість функцій каскадної активації або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_get\_cascade\_activation\_functions()](function.fann-get-cascade-activation-functions.md) \- Повертає функції каскадної активації
-   [fann\_set\_cascade\_activation\_functions()](function.fann-set-cascade-activation-functions.md) \- встановлює масив каскадних функцій активації кандидатів
