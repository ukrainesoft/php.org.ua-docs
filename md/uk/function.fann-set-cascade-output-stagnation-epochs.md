---
navigation:
  - function.fann-set-cascade-output-change-fraction.md: « fann\_set\_cascade\_output\_change\_fraction
  - function.fann-set-cascade-weight-multiplier.md: fann\_set\_cascade\_weight\_multiplier »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_cascade\_output\_stagnation\_epochs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_cascade\_output\_stagnation\_epochs

(PECL fann >= 1.0.0)

fann\_set\_cascade\_output\_stagnation\_epochs - Встановлює кількість періодів стагнації каскадного виводу

### Опис

```methodsynopsis
fann_set_cascade_output_stagnation_epochs(resource $ann, int $cascade_output_stagnation_epochs): bool
```

Встановлює кількість періодів стагнації каскадного виведення.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_output_stagnation_epochs`

Кількість епох стагнації каскадного виходу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_cascade\_output\_stagnation\_epochs()](function.fann-get-cascade-output-stagnation-epochs.md) \- Повертає кількість каскадних періодів застою кандидатів
