---
navigation:
  - function.fann-cascadetrain-on-data.md: « fann\_cascadetrain\_on\_data
  - function.fann-clear-scaling-params.md: fann\_clear\_scaling\_params »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_cascadetrain\_on\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_cascadetrain\_on\_file

(PECL fann >= 1.0.0)

fann\_cascadetrain\_on\_file — Навчання на даних прочитаних із файлу за допомогою алгоритму Cascade2

### Опис

```methodsynopsis
fann_cascadetrain_on_file(    resource $ann,    string $filename,    int $max_neurons,    int $neurons_between_reports,    float $desired_error): bool
```

Робить те саме, що і [fann\_cascadetrain\_on\_data()](function.fann-cascadetrain-on-data.md)але читає дані безпосередньо з файлу.

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

Вибрані [fann\_get\_MSE()](function.fann-get-mse.md) або [fann\_get\_bit\_fail()](function.fann-get-bit-fail.md), в залежності від обраної за допомогою [fann\_set\_train\_stop\_function()](function.fann-set-train-stop-function.md)функции остановки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_train\_on\_data()](function.fann-train-on-data.md) \- Навчання на всьому обсязі даних на часовому інтервалі
-   [fann\_cascadetrain\_on\_data()](function.fann-cascadetrain-on-data.md) \- Навчання на всьому наборі даних протягом певного періоду часу за допомогою алгоритму Cascade2
