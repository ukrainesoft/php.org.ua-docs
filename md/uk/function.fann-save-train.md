---
navigation:
  - function.fann-run.md: « fann\_run
  - function.fann-save.md: fann\_save »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_save\_train
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_save\_train

(PECL fann >= 1.0.0)

fann\_save\_train — Зберігає структуру навчання у файл

### Опис

```methodsynopsis
fann_save_train(resource $data, string $file_name): bool
```

Зберігає дані навчання у файл у форматі, вказаному в [fann\_read\_train\_from\_file()](function.fann-read-train-from-file.md)

### Список параметрів

`data`

Ресурс (resource) навчальних даних нейронної мережі.

`file_name`

Ім'я файлу, у якому зберігаються дані навчання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_read\_train\_from\_file()](function.fann-read-train-from-file.md) \- Читає файл, у якому зберігаються дані навчання
