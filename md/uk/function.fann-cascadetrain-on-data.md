Навчання по всьому набору даних протягом певного періоду часу за допомогою алгоритму Cascade2

-   [« Функции Fann](ref.fann.html)
    
-   [fann\_cascadetrain\_on\_file »](function.fann-cascadetrain-on-file.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Навчання по всьому набору даних протягом певного періоду часу за допомогою алгоритму Cascade2
    

# fanncascadetrainвінdata

(PECL fann> = 1.0.0)

fanncascadetrainвінdata — Навчання по всьому набору даних протягом певного періоду часу за допомогою алгоритму Cascade2

### Опис

```methodsynopsis
fann_cascadetrain_on_data(    resource $ann,    resource $data,    int $max_neurons,    int $neurons_between_reports,    float $desired_error): bool
```

Фракція каскадного виведення є числом від 0 до 1 і визначає, наскільки сильно має змінитися значення [fann\_get\_MSE()](function.fann-get-mse.html) в [fann\_get\_cascade\_output\_stagnation\_epochs()](function.fann-get-cascade-output-stagnation-epochs.html) під час навчання вихідних з'єднань, щоб навчання не стагнувало. Якщо навчання стагнувало, навчання вихідних з'єднань буде завершено і будуть підготовлені нові кандидати.

Це навчання використовує параметри, встановлені fannsetcascade..., але також воно використовує інший навчальний алгоритм як внутрішній навчальний алгоритм. Цей алгоритм може бути заданий як **`FANN_TRAIN_RPROP`** або **`FANN_TRAIN_QUICKPROP`** за допомогою [fann\_set\_training\_algorithm()](function.fann-set-training-algorithm.html), і параметри, задані цих навчальних алгоритмів, також враховуватимуться в каскадному навчанні.

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

Бажана [fann\_get\_MSE()](function.fann-get-mse.html) або [fann\_get\_bit\_fail()](function.fann-get-bit-fail.html), в залежності від обраної за допомогою [fann\_set\_train\_stop\_function()](function.fann-set-train-stop-function.html) зупинної функції.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_train\_on\_data()](function.fann-train-on-data.html) - Навчання на всьому обсязі даних на часовому інтервалі
-   [fann\_cascadetrain\_on\_file()](function.fann-cascadetrain-on-file.html) - Навчання на даних прочитаних із файлу за допомогою алгоритму Cascade2