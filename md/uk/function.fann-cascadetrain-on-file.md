---
navigation:
  - function.fann-cascadetrain-on-data.md: « fanncascadetrainвінdata
  - function.fann-clear-scaling-params.md: fannclearscalingparams »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanncascadetrainвінfile
---
# fanncascadetrainвінfile

(PECL fann> = 1.0.0)

fanncascadetrainвінfile — Навчання на даних прочитаних із файлу за допомогою алгоритму Cascade2

### Опис

```methodsynopsis
fann_cascadetrain_on_file(    resource $ann,    string $filename,    int $max_neurons,    int $neurons_between_reports,    float $desired_error): bool
```

Робить те саме, що і [fanncascadetrainвінdata()](function.fann-cascadetrain-on-data.md)але читає дані безпосередньо з файлу.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`filename`

Файл із даними.

`max_neurons`

Максимальна кількість нейронів у мережі.

`neurons_between_reports`

Кількість нейронів між виведенням звітів про стан. Якщо задати 0, то звіти не друкуватимуться.

`desired_error`

Вибрані [fanngetMSE()](function.fann-get-mse.md) або [fanngetbitfail()](function.fann-get-bit-fail.md), в залежності від обраної за допомогою [fannsettrainstopfunction()](function.fann-set-train-stop-function.md) функції зупинки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanntrainвінdata()](function.fann-train-on-data.md) - Навчання на всьому обсязі даних на часовому інтервалі
-   [fanncascadetrainвінdata()](function.fann-cascadetrain-on-data.md) - Навчання на всьому наборі даних протягом певного періоду часу за допомогою алгоритму Cascade2
