---
navigation:
  - function.fann-train-on-data.md: « fann\_train\_on\_data
  - function.fann-train.md: fann\_train »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_train\_on\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_train\_on\_file

(PECL fann >= 1.0.0)

fann\_train\_on\_file — Навчання на повному наборі даних, прочитаному з файлу, на часовому інтервалі

### Опис

```methodsynopsis
fann_train_on_file(    resource $ann,    string $filename,    int $max_epochs,    int $epochs_between_reports,    float $desired_error): bool
```

Навчання на повному наборі даних, прочитаному із файлу, на часовому інтервалі.

Це навчання використовує алгоритм, вибраний функцією [fann\_set\_training\_algorithm()](function.fann-set-training-algorithm.md) та набір параметрів для цих алгоритмів.

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

Бажана [fann\_get\_MSE()](function.fann-get-mse.md) або [fann\_get\_bit\_fail()](function.fann-get-bit-fail.md), в залежності від обраної функції зупинки [fann\_set\_train\_stop\_function()](function.fann-set-train-stop-function.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_train\_on\_data()](function.fann-train-on-data.md) \- Навчання на всьому обсязі даних на часовому інтервалі
-   [fann\_train\_epoch()](function.fann-train-epoch.md) \- Навчання протягом однієї епохи
-   [fann\_get\_bit\_fail()](function.fann-get-bit-fail.md) \- Кількість бітів збою
-   [fann\_get\_MSE()](function.fann-get-mse.md) \- Зчитує середньоквадратичну помилку мережі
-   [fann\_set\_train\_stop\_function()](function.fann-set-train-stop-function.md) \- Встановлює функцію зупинки під час тренування.
-   [fann\_set\_training\_algorithm()](function.fann-set-training-algorithm.md) \- встановлює алгоритм навчання
-   [fann\_set\_callback()](function.fann-set-callback.md) \- Встановлює callback-функцію для використання під час навчання
