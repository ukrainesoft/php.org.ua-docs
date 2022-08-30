Навчання на всьому обсязі даних на часовому інтервалі

-   [« fanntrainepoch](function.fann-train-epoch.html)
    
-   [fanntrainвінfile »](function.fann-train-on-file.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Fann](ref.fann.md)
    
-   Навчання на всьому обсязі даних на часовому інтервалі
    

# fanntrainвінdata

(PECL fann> = 1.0.0)

fanntrainвінdata — Навчання на всьому обсязі даних на часовому інтервалі

### Опис

```methodsynopsis
fann_train_on_data(    resource $ann,    resource $data,    int $max_epochs,    int $epochs_between_reports,    float $desired_error): bool
```

Навчання на повному наборі даних, часовому інтервалі.

Це навчання використовує алгоритм, вибраний функцією [fannsettrainingalgorithm()](function.fann-set-training-algorithm.html) та набір параметрів для цих алгоритмів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`data`

Ресурс (resource) навчальних даних нейронної мережі.

`max_epochs`

Максимальна кількість епох, яка має тривати навчання

`epochs_between_reports`

Кількість епох між викликами користувальницької функції. Якщо дорівнює нулю, то функція не запускатиметься.

`desired_error`

Бажана [fanngetMSE()](function.fann-get-mse.html) або [fanngetbitfail()](function.fann-get-bit-fail.html), в залежності від обраної функції зупинки [fannsettrainstopfunction()](function.fann-set-train-stop-function.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanntrainвінfile()](function.fann-train-on-file.html) - Навчання на повному наборі даних, прочитаному з файлу, на часовому інтервалі
-   [fanntrainepoch()](function.fann-train-epoch.html) - Навчання протягом однієї епохи
-   [fanngetbitfail()](function.fann-get-bit-fail.html) - Кількість бітів збою
-   [fanngetMSE()](function.fann-get-mse.html) - Зчитує середньоквадратичну помилку мережі
-   [fannsettrainstopfunction()](function.fann-set-train-stop-function.html) - Встановлює функцію зупинки під час тренування.
-   [fannsettrainingalgorithm()](function.fann-set-training-algorithm.html) - встановлює алгоритм навчання
-   [fannsetcallback()](function.fann-set-callback.html) - Встановлює callback-функцію для використання під час навчання