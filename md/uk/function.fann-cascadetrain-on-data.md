---
navigation:
  - ref.fann.md: « Функции Fann
  - function.fann-cascadetrain-on-file.md: fanncascadetrainвінfile »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanncascadetrainвінdata
---
# fanncascadetrainвінdata

(PECL fann> = 1.0.0)

fanncascadetrainвінdata — Навчання по всьому набору даних протягом певного періоду часу за допомогою алгоритму Cascade2

### Опис

```methodsynopsis
fann_cascadetrain_on_data(    resource $ann,    resource $data,    int $max_neurons,    int $neurons_between_reports,    float $desired_error): bool
```

Фракція каскадного виведення є числом від 0 до 1 і визначає, наскільки сильно має змінитися значення [fanngetMSE()](function.fann-get-mse.md) в [fanngetcascadeoutputstagnationepochs()](function.fann-get-cascade-output-stagnation-epochs.md) під час навчання вихідних з'єднань, щоб навчання не стагнувало. Якщо навчання стагнувало, навчання вихідних з'єднань буде завершено і будуть підготовлені нові кандидати.

Це навчання використовує параметри, встановлені fannsetcascade..., але також воно використовує інший навчальний алгоритм як внутрішній навчальний алгоритм. Цей алгоритм може бути заданий як **`FANN_TRAIN_RPROP`** або **`FANN_TRAIN_QUICKPROP`** за допомогою [fannsettrainingalgorithm()](function.fann-set-training-algorithm.md), і параметри, задані цих навчальних алгоритмів, також враховуватимуться в каскадному навчанні.

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

Бажана [fanngetMSE()](function.fann-get-mse.md) або [fanngetbitfail()](function.fann-get-bit-fail.md), в залежності від обраної за допомогою [fannsettrainstopfunction()](function.fann-set-train-stop-function.md) зупинної функції.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanntrainвінdata()](function.fann-train-on-data.md) - Навчання на всьому обсязі даних на часовому інтервалі
-   [fanncascadetrainвінfile()](function.fann-cascadetrain-on-file.md) - Навчання на даних прочитаних із файлу за допомогою алгоритму Cascade2
