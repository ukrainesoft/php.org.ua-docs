---
navigation:
  - function.fann-get-cascade-activation-functions.md: « fann\_get\_cascade\_activation\_functions
  - function.fann-get-cascade-activation-steepnesses.md: fann\_get\_cascade\_activation\_steepnesses »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_cascade\_activation\_steepnesses\_count
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_cascade\_activation\_steepnesses\_count

(PECL fann >= 1.0.0)

fann\_get\_cascade\_activation\_steepnesses\_count — Кількість крутості активації

### Опис

```methodsynopsis
fann_get_cascade_activation_steepnesses_count(resource $ann): int
```

Кількість крутості активації в масиві [fann\_get\_cascade\_activation\_functions()](function.fann-get-cascade-activation-functions.md)

Кількість крутості активації за замовчуванням – 4.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Кількість крутості активації або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_get\_cascade\_activation\_steepnesses()](function.fann-get-cascade-activation-steepnesses.md) \- Повертає крутість каскадної активації
-   [fann\_set\_cascade\_activation\_functions()](function.fann-set-cascade-activation-functions.md) \- встановлює масив каскадних функцій активації кандидатів
