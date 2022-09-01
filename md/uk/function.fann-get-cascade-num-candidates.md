---
navigation:
  - function.fann-get-cascade-num-candidate-groups.html: « fanngetcascadenumcandidategroups
  - function.fann-get-cascade-output-change-fraction.html: fanngetcascadeoutputchangefraction »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fanngetcascadenumcandidates
---
# fanngetcascadenumcandidates

(PECL fann> = 1.0.0)

fanngetcascadenumcandidates — Повертає кількість кандидатів, використаних під час навчання

### Опис

```methodsynopsis
fann_get_cascade_num_candidates(resource $ann): int
```

Кількість кандидатів, використаних під час навчання (розраховується шляхом перемноження [fanngetcascadeactivationfunctionscount()](function.fann-get-cascade-activation-functions-count.html) [fanngetcascadeactivationsteepnessescount()](function.fann-get-cascade-activation-steepnesses-count.html) і [fanngetcascadenumcandidategroups()](function.fann-get-cascade-num-candidate-groups.html)

Фактичні кандидати визначаються масивами [fanngetcascadeactivationfunctions()](function.fann-get-cascade-activation-functions.html) і [fanngetcascadeactivationsteepnesses()](function.fann-get-cascade-activation-steepnesses.html). Ці масиви визначають функції активації та крутості активації, що використовуються для нейронів-кандидатів. Якщо є 2 функції активації у масиві функцій активації та 3 крутості у масиві крутості, тоді буде 2 x 3 = 6 різних кандидатів, які будуть навчені. Ці 6 різних кандидатів можуть бути скопійовані в кілька груп кандидатів, де єдина різниця між цими групами - початкові ваги. Якщо кількість груп дорівнює 2, кількість нейронів-кандидатів буде 2 x 3 x 2 = 12. Кількість груп кандидатів визначається [fannsetcascadenumcandidategroups()](function.fann-set-cascade-num-candidate-groups.html)

Кількість кандидатів за умовчанням – 6 x 4 x 2 = 48.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Кількість кандидатів, використаних під час навчання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fanngetcascadeactivationfunctions()](function.fann-get-cascade-activation-functions.html) - Повертає функції каскадної активації
-   [fanngetcascadeactivationfunctionscount()](function.fann-get-cascade-activation-functions-count.html) - Повертає кількість функцій каскадної активації
-   [fanngetcascadeactivationsteepnesses()](function.fann-get-cascade-activation-steepnesses.html) - Повертає крутість каскадної активації
-   [fanngetcascadeactivationsteepnessescount()](function.fann-get-cascade-activation-steepnesses-count.html) - Кількість крутості активації
-   [fanngetcascadenumcandidategroups()](function.fann-get-cascade-num-candidate-groups.html) - Повертає кількість груп кандидатів
