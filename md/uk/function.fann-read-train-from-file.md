---
navigation:
  - function.fann-randomize-weights.md: « fann\_randomize\_weights
  - function.fann-reset-errno.md: fann\_reset\_errno »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_read\_train\_from\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_read\_train\_from\_file

(PECL fann >= 1.0.0)

fann\_read\_train\_from\_file — Читає файл, у якому зберігаються дані навчання

### Опис

```methodsynopsis
fann_read_train_from_file(string $filename): resource
```

Читає файл, де зберігаються дані навчання.

### Список параметрів

`filename`

Вхідний файл у наступному форматі:

num\_train\_data num\_input num\_output вхідні дані, розділені пропуском вихідні дані, розділені пропуском

. . .

вхідні дані, розділені пропуском вихідні дані, розділені пропуском

### Значення, що повертаються

Повертає ресурс (resource) навчальних даних, або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** fann\_read\_train\_from\_file()\*\*\*\*

```php
<?php
$train_data = fann_read_train_from_file("xor.data");
if ($train_data) {
    // Сделайте что-нибудь с $train_data для функции XOR
}
?>
```

Вміст xor.data

4 2 1 -1 -1 -1 -1 1 1 1 -1 1 1 1 -1

### Дивіться також

-   [fann\_train\_on\_data()](function.fann-train-on-data.md) \- Навчання на всьому обсязі даних на часовому інтервалі
-   [fann\_destroy\_train()](function.fann-destroy-train.md) \- Знищує тренувальні дані
-   [fann\_save\_train()](function.fann-save-train.md) \- Зберігає структуру навчання у файл
