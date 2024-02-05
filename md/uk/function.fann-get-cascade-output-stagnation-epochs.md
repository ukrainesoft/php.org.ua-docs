---
navigation:
  - function.fann-get-cascade-output-change-fraction.md: « fann\_get\_cascade\_output\_change\_fraction
  - function.fann-get-cascade-weight-multiplier.md: fann\_get\_cascade\_weight\_multiplier »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_cascade\_output\_stagnation\_epochs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_cascade\_output\_stagnation\_epochs

(PECL fann >= 1.0.0)

fann\_get\_cascade\_output\_stagnation\_epochs - Повертає кількість каскадних періодів застою кандидатів

### Опис

```methodsynopsis
fann_get_cascade_output_stagnation_epochs(resource $ann): int
```

Кількість каскадних періодів застою кандидатів визначає кількість періодів навчання, яка буде продовжена без зміни оцінки MSE за допомогою [fann\_get\_cascade\_output\_change\_fraction()](function.fann-get-cascade-output-change-fraction.md)

Дивіться додаткову інформацію про цей параметр у [fann\_get\_cascade\_output\_change\_fraction()](function.fann-get-cascade-output-change-fraction.md)

За замовчуванням кількість періодів застою каскадного виводу дорівнює 12.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Кількість каскадних періодів застою кандидатів або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_cascade\_output\_stagnation\_epochs()](function.fann-set-cascade-output-stagnation-epochs.md) \- встановлює кількість періодів стагнації каскадного виводу
-   [fann\_get\_cascade\_output\_change\_fraction()](function.fann-get-cascade-output-change-fraction.md) \- Повертає частку зміни виходу каскаду
