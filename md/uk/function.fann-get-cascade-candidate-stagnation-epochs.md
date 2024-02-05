---
navigation:
  - function.fann-get-cascade-candidate-limit.md: « fann\_get\_cascade\_candidate\_limit
  - function.fann-get-cascade-max-cand-epochs.md: fann\_get\_cascade\_max\_cand\_epochs »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_cascade\_candidate\_stagnation\_epochs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_cascade\_candidate\_stagnation\_epochs

(PECL fann >= 1.0.0)

fann\_get\_cascade\_candidate\_stagnation\_epochs - Повертає кількість періодів застою каскаду кандидата

### Опис

```methodsynopsis
fann_get_cascade_candidate_stagnation_epochs(resource $ann): int
```

Кількість періодів застою каскаду кандидата визначає кількість періодів, яким дозволено продовжити навчання без зміни MSE на частку [fann\_get\_cascade\_candidate\_change\_fraction()](function.fann-get-cascade-candidate-change-fraction.md)

Дивіться додаткову інформацію про цей параметр у [fann\_get\_cascade\_candidate\_change\_fraction()](function.fann-get-cascade-candidate-change-fraction.md)

За замовчуванням кількість періодів застою каскаду кандидата дорівнює 12.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Количество периодов застоя каскада кандидата или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_cascade\_candidate\_stagnation\_epochs()](function.fann-set-cascade-candidate-stagnation-epochs.md) \- встановлює кількість каскадних періодів застою кандидатів
-   [fann\_get\_cascade\_candidate\_change\_fraction()](function.fann-get-cascade-candidate-change-fraction.md) \- Повертає частку зміни каскаду кандидата
