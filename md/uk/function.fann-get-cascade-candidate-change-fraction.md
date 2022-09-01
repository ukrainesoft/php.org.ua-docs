---
navigation:
  - function.fann-get-cascade-activation-steepnesses.html: « fanngetcascadeactivationsteepnesses
  - function.fann-get-cascade-candidate-limit.html: fanngetcascadecandidatelimit »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetcascadecandidatechangefraction
---
# fanngetcascadecandidatechangefraction

(PECL fann> = 1.0.0)

fanngetcascadecandidatechangefraction - Повертає частку зміни каскаду кандидата

### Опис

```methodsynopsis
fann_get_cascade_candidate_change_fraction(resource $ann): float
```

Частка зміни каскаду кандидата - це число від 0 до 1, що визначає, наскільки велике значення [fanngetMSE()](function.fann-get-mse.html), що має змінитися в межах [fanngetcascadecandidatestagnationepochs()](function.fann-get-cascade-candidate-stagnation-epochs.md) під час навчання нейронів-кандидатів, щоби навчання не застоювалося. Якщо навчання застоюється, навчання нейронів-кандидатів припиняється і вибирається найкращий кандидат.

Це означає, що якщо MSE не змінюється на частку **fanngetcascadecandidatechangefraction()** протягом періоду [fanngetcascadecandidatestagnationepochs()](function.fann-get-cascade-candidate-stagnation-epochs.md), навчання нейронів-кандидатів припиняється, тому що навчання зупинилося.

Якщо частка зміни каскаду кандидатів мала, нейрони-кандидати навчатимуться більше, і якщо частка висока, вони навчатимуться менше.

Частка зміни каскаду за замовчуванням кандидата становить 0.01, що еквівалентно зміні MSE на 1%.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Частка зміни каскаду кандидата або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsetcascadecandidatechangefraction()](function.fann-set-cascade-candidate-change-fraction.md) - встановлює частку каскадної зміни кандидата
-   [fanngetMSE()](function.fann-get-mse.md) - Зчитує середньоквадратичну помилку мережі
-   [fanngetcascadecandidatestagnationepochs()](function.fann-get-cascade-candidate-stagnation-epochs.md) - Повертає кількість періодів застою каскаду кандидата
