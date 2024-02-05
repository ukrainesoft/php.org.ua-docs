---
navigation:
  - function.fann-set-bit-fail-limit.md: « fann\_set\_bit\_fail\_limit
  - function.fann-set-cascade-activation-functions.md: fann\_set\_cascade\_activation\_functions »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_callback
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_callback

(PECL fann >= 1.0.0)

fann\_set\_callback - Встановлює callback-функцію для використання під час навчання

### Опис

```methodsynopsis
fann_set_callback(resource $ann, callable $callback): bool
```

Встановлює callback-функцію використання під час навчання. Це означає, що вона викликається з [fann\_train\_on\_data()](function.fann-train-on-data.md) або [fann\_train\_on\_file()](function.fann-train-on-file.md)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`callback`

Callback-функція, що поставляється, приймає наступні параметри:

-   `ann`\- Ресурс (resource) нейронної мережі
-   `train`\- ресурс даних для навчання або\*\*`null`\*\*, якщо викликається з[fann\_train\_on\_file()](function.fann-train-on-file.md)
-   `max_epochs`\- Максимальна кількість періодів, у яких має продовжуватися навчання
-   `epochs_between_reports`\- Кількість періодів між викликами цієї функції
-   `desired_error`\- Бажана функція[fann\_get\_MSE()](function.fann-get-mse.md) або [fann\_get\_bit\_fail()](function.fann-get-bit-fail.md), залежно від функції зупинки, вибраної[fann\_set\_train\_stop\_function()](function.fann-set-train-stop-function.md)
-   `epochs`\- Поточний період

Callback-функція має повернути **`true`**. Якщо вона поверне **`false`**, навчання буде припинено.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_train\_on\_data()](function.fann-train-on-data.md) \- Навчання на всьому обсязі даних на часовому інтервалі
-   [fann\_train\_on\_file()](function.fann-train-on-file.md) \- Навчання на повному наборі даних, прочитаному з файлу, на часовому інтервалі
