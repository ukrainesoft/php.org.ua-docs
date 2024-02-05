---
navigation:
  - ref.fann.md: « Функції Fann
  - function.fann-cascadetrain-on-file.md: fann\_cascadetrain\_on\_file »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_cascadetrain\_on\_data
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_cascadetrain\_on\_data

(PECL fann >= 1.0.0)

fann\_cascadetrain\_on\_data — Навчання по всьому набору даних протягом певного періоду часу за допомогою алгоритму Cascade2

### Опис

```methodsynopsis
fann_cascadetrain_on_data(    resource $ann,    resource $data,    int $max_neurons,    int $neurons_between_reports,    float $desired_error): bool
```

Фракція каскадного виведення є числом від 0 до 1 і визначає, наскільки сильно має змінитися значення [fann\_get\_MSE()](function.fann-get-mse.md)в[fann\_get\_cascade\_output\_stagnation\_epochs()](function.fann-get-cascade-output-stagnation-epochs.md) під час навчання вихідних з'єднань, щоб навчання не стагнувало. Якщо навчання стагнувало, навчання вихідних з'єднань буде завершено і будуть підготовлені нові кандидати.

Це навчання використовує параметри, встановлені fann\_set\_cascade\_..., але також воно використовує інший навчальний алгоритм як внутрішній навчальний алгоритм. Цей алгоритм може бути заданий як **`FANN_TRAIN_RPROP`** або **`FANN_TRAIN_QUICKPROP`** за допомогою [fann\_set\_training\_algorithm()](function.fann-set-training-algorithm.md), та параметри, задані для цих навчальних алгоритмів, також враховуватимуться в каскадному навчанні.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`data`

Ресурс (resource) навчальних даних нейронної мережі.

`max_neurons`

Максимальна кількість нейронів для додавання до мережі.

`neurons_between_reports`

Друк звіту про статус відбуватиметься через задане в цьому параметрі число нейронів. Якщо заданий нуль, то друк не відбуватиметься.

`desired_error`

Бажана [fann\_get\_MSE()](function.fann-get-mse.md) або [fann\_get\_bit\_fail()](function.fann-get-bit-fail.md), в залежності від обраної за допомогою [fann\_set\_train\_stop\_function()](function.fann-set-train-stop-function.md)остановочной функции.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_train\_on\_data()](function.fann-train-on-data.md) \- Навчання на всьому обсязі даних на часовому інтервалі
-   [fann\_cascadetrain\_on\_file()](function.fann-cascadetrain-on-file.md) \- Навчання на даних прочитаних із файлу за допомогою алгоритму Cascade2
