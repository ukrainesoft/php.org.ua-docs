---
navigation:
  - function.fann-get-cascade-activation-steepnesses-count.md: « fann\_get\_cascade\_activation\_steepnesses\_count
  - function.fann-get-cascade-candidate-change-fraction.md: fann\_get\_cascade\_candidate\_change\_fraction »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_cascade\_activation\_steepnesses
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_cascade\_activation\_steepnesses

(PECL fann >= 1.0.0)

fann\_get\_cascade\_activation\_steepnesses — Повертає крутість каскадної активації

### Опис

```methodsynopsis
fann_get_cascade_activation_steepnesses(resource $ann): array
```

Масив крутості каскадної активації – це масив різних функцій активації, які використовуються кандидатами.

Смотрите[fann\_get\_cascade\_num\_candidates()](function.fann-get-cascade-num-candidates.md) для опису того, які кандидатні нейрони генеруватимуться цим масивом.

Крутизна активації за промовчанням: {0,25, 0,50, 0,75, 1,00}.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Крутизна каскадної активації або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_get\_cascade\_activation\_steepnesses\_count()](function.fann-get-cascade-activation-steepnesses-count.md) \- Кількість крутості активації
-   [fann\_set\_cascade\_activation\_steepnesses()](function.fann-set-cascade-activation-steepnesses.md) \- Встановлює масив крутості включення кандидатів у каскад
