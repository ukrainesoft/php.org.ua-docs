Навчання на даних прочитаних із файлу за допомогою алгоритму Cascade2

-   [« fann\_cascadetrain\_on\_data](function.fann-cascadetrain-on-data.html)
    
-   [fann\_clear\_scaling\_params »](function.fann-clear-scaling-params.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Навчання на даних прочитаних із файлу за допомогою алгоритму Cascade2
    

# fanncascadetrainвінfile

(PECL fann> = 1.0.0)

fanncascadetrainвінfile — Навчання на даних прочитаних із файлу за допомогою алгоритму Cascade2

### Опис

```methodsynopsis
fann_cascadetrain_on_file(    resource $ann,    string $filename,    int $max_neurons,    int $neurons_between_reports,    float $desired_error): bool
```

Робить те саме, що і [fann\_cascadetrain\_on\_data()](function.fann-cascadetrain-on-data.html)але читає дані безпосередньо з файлу.

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

Вибрані [fann\_get\_MSE()](function.fann-get-mse.html) або [fann\_get\_bit\_fail()](function.fann-get-bit-fail.html), в залежності від обраної за допомогою [fann\_set\_train\_stop\_function()](function.fann-set-train-stop-function.html) функції зупинки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_train\_on\_data()](function.fann-train-on-data.html) - Навчання на всьому обсязі даних на часовому інтервалі
-   [fann\_cascadetrain\_on\_data()](function.fann-cascadetrain-on-data.html) - Навчання на всьому наборі даних протягом певного періоду часу за допомогою алгоритму Cascade2