---
navigation:
  - function.fann-run.html: « fannrun
  - function.fann-save.html: fannsave »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsavetrain
---
# fannsavetrain

(PECL fann> = 1.0.0)

fannsavetrain — Зберігає структуру навчання у файл

### Опис

```methodsynopsis
fann_save_train(resource $data, string $file_name): bool
```

Зберігає дані навчання у файл у форматі, вказаному в [fannreadtrainfromfile()](function.fann-read-train-from-file.html)

### Список параметрів

`data`

Ресурс (resource) навчальних даних нейронної мережі.

`file_name`

Ім'я файлу, у якому зберігаються дані навчання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fannreadtrainfromfile()](function.fann-read-train-from-file.html) - Читає файл, у якому зберігаються дані навчання
