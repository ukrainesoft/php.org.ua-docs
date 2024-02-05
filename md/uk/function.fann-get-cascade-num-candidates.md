---
navigation:
  - function.fann-get-cascade-num-candidate-groups.md: « fann\_get\_cascade\_num\_candidate\_groups
  - function.fann-get-cascade-output-change-fraction.md: fann\_get\_cascade\_output\_change\_fraction »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_cascade\_num\_candidates
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_cascade\_num\_candidates

(PECL fann >= 1.0.0)

fann\_get\_cascade\_num\_candidates — Повертає кількість кандидатів, використаних під час навчання

### Опис

```methodsynopsis
fann_get_cascade_num_candidates(resource $ann): int
```

Кількість кандидатів, використаних під час навчання (розраховується шляхом перемноження [fann\_get\_cascade\_activation\_functions\_count()](function.fann-get-cascade-activation-functions-count.md) [fann\_get\_cascade\_activation\_steepnesses\_count()](function.fann-get-cascade-activation-steepnesses-count.md) і [fann\_get\_cascade\_num\_candidate\_groups()](function.fann-get-cascade-num-candidate-groups.md)

Фактичні кандидати визначаються масивами [fann\_get\_cascade\_activation\_functions()](function.fann-get-cascade-activation-functions.md) і [fann\_get\_cascade\_activation\_steepnesses()](function.fann-get-cascade-activation-steepnesses.md). Ці масиви визначають функції активації та крутості активації, що використовуються для нейронів-кандидатів. Якщо є 2 функції активації у масиві функцій активації та 3 крутості у масиві крутості, тоді буде 2 x 3 = 6 різних кандидатів, які будуть навчені. Ці 6 різних кандидатів можуть бути скопійовані в кілька груп кандидатів, де єдина різниця між цими групами - початкові ваги. Якщо кількість груп дорівнює 2, кількість нейронів-кандидатів буде 2 x 3 x 2 = 12. Кількість груп кандидатів визначається [fann\_set\_cascade\_num\_candidate\_groups()](function.fann-set-cascade-num-candidate-groups.md)

Кількість кандидатів за умовчанням – 6 x 4 x 2 = 48.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Кількість кандидатів, використаних під час навчання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_get\_cascade\_activation\_functions()](function.fann-get-cascade-activation-functions.md) \- Повертає функції каскадної активації
-   [fann\_get\_cascade\_activation\_functions\_count()](function.fann-get-cascade-activation-functions-count.md) \- Повертає кількість функцій каскадної активації
-   [fann\_get\_cascade\_activation\_steepnesses()](function.fann-get-cascade-activation-steepnesses.md) \- Повертає крутість каскадної активації
-   [fann\_get\_cascade\_activation\_steepnesses\_count()](function.fann-get-cascade-activation-steepnesses-count.md) \- Кількість крутості активації
-   [fann\_get\_cascade\_num\_candidate\_groups()](function.fann-get-cascade-num-candidate-groups.md) \- Повертає кількість груп кандидатів
