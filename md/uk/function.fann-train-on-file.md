---
navigation:
  - function.fann-train-on-data.html: « fanntrainвінdata
  - function.fann-train.html: fanntrain »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanntrainвінfile
---
# fanntrainвінfile

(PECL fann> = 1.0.0)

fanntrainвінfile — Навчання на повному наборі даних, прочитаному з файлу, на часовому інтервалі

### Опис

```methodsynopsis
fann_train_on_file(    resource $ann,    string $filename,    int $max_epochs,    int $epochs_between_reports,    float $desired_error): bool
```

Навчання на повному наборі даних, прочитаному із файлу, на часовому інтервалі.

Це навчання використовує алгоритм, вибраний функцією [fannsettrainingalgorithm()](function.fann-set-training-algorithm.md) та набір параметрів для цих алгоритмів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`filename`

Файл, який містить навчальні дані

`max_epochs`

Максимальна кількість епох, яка має тривати навчання

`epochs_between_reports`

Кількість епох між викликами користувальницької функції. Якщо дорівнює нулю, то функція не запускатиметься.

`desired_error`

Бажана [fanngetMSE()](function.fann-get-mse.html) або [fanngetbitfail()](function.fann-get-bit-fail.html), залежно від обраної функції зупинки [fannsettrainstopfunction()](function.fann-set-train-stop-function.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanntrainвінdata()](function.fann-train-on-data.md) - Навчання на всьому обсязі даних на часовому інтервалі
-   [fanntrainepoch()](function.fann-train-epoch.md) - Навчання протягом однієї епохи
-   [fanngetbitfail()](function.fann-get-bit-fail.md) - Кількість бітів збою
-   [fanngetMSE()](function.fann-get-mse.md) - Зчитує середньоквадратичну помилку мережі
-   [fannsettrainstopfunction()](function.fann-set-train-stop-function.md) - Встановлює функцію зупинки під час тренування.
-   [fannsettrainingalgorithm()](function.fann-set-training-algorithm.md) - встановлює алгоритм навчання
-   [fannsetcallback()](function.fann-set-callback.md) - Встановлює callback-функцію для використання під час навчання
