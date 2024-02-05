---
navigation:
  - function.fann-get-cascade-activation-steepnesses.md: « fann\_get\_cascade\_activation\_steepnesses
  - function.fann-get-cascade-candidate-limit.md: fann\_get\_cascade\_candidate\_limit »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_cascade\_candidate\_change\_fraction
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_cascade\_candidate\_change\_fraction

(PECL fann >= 1.0.0)

fann\_get\_cascade\_candidate\_change\_fraction - Повертає частку зміни каскаду кандидата

### Опис

```methodsynopsis
fann_get_cascade_candidate_change_fraction(resource $ann): float
```

Частка зміни каскаду кандидата - це число від 0 до 1, що визначає, наскільки велике значення [fann\_get\_MSE()](function.fann-get-mse.md), що має змінитися в межах [fann\_get\_cascade\_candidate\_stagnation\_epochs()](function.fann-get-cascade-candidate-stagnation-epochs.md) під час навчання нейронів-кандидатів, щоби навчання не застоювалося. Якщо навчання застоюється, навчання нейронів-кандидатів припиняється і вибирається найкращий кандидат.

Це означає, що якщо MSE не змінюється на частку \*\*fann\_get\_cascade\_candidate\_change\_fraction()\*\*в течение периода[fann\_get\_cascade\_candidate\_stagnation\_epochs()](function.fann-get-cascade-candidate-stagnation-epochs.md), навчання нейронів-кандидатів припиняється, тому що навчання зупинилося.

Якщо частка зміни каскаду кандидатів мала, нейрони-кандидати навчатимуться більше, і якщо частка висока, вони навчатимуться менше.

Частка зміни каскаду за замовчуванням кандидата становить 0.01, що еквівалентно зміні MSE на 1%.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Доля изменения каскада кандидата или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_cascade\_candidate\_change\_fraction()](function.fann-set-cascade-candidate-change-fraction.md) \- встановлює частку каскадної зміни кандидата
-   [fann\_get\_MSE()](function.fann-get-mse.md) \- Зчитує середньоквадратичну помилку мережі
-   [fann\_get\_cascade\_candidate\_stagnation\_epochs()](function.fann-get-cascade-candidate-stagnation-epochs.md) \- Повертає кількість періодів застою каскаду кандидата
