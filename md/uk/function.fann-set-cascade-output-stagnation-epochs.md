---
navigation:
  - function.fann-set-cascade-output-change-fraction.html: « fannsetcascadeoutputchangefraction
  - function.fann-set-cascade-weight-multiplier.html: fannsetcascadeweightmultiplier »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetcascadeoutputstagnationepochs
---
# fannsetcascadeoutputstagnationepochs

(PECL fann> = 1.0.0)

fannsetcascadeoutputstagnationepochs - Встановлює кількість періодів стагнації каскадного виводу

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

-   [fanngetcascadeoutputstagnationepochs()](function.fann-get-cascade-output-stagnation-epochs.html) - Повертає кількість каскадних періодів застою кандидатів
