---
navigation:
  - function.gzopen.md: « gzopen
  - function.gzputs.md: gzputs »
  - index.md: PHP Manual
  - ref.zlib.md: Функции Zlib
title: gzpassthru
---
# gzpassthru

(PHP 4, PHP 5, PHP 7, PHP 8)

gzpassthru — Виведення всіх даних, що залишилися, з покажчика gz-файлу.

### Опис

```methodsynopsis
gzpassthru(resource $stream): int
```

Читає до кінця файлу (EOF) дані з покажчика gz-файлу, починаючи з поточної позиції, і записує результат (без стиснення) стандартний висновок.

> **Зауваження**
> 
> Використовуйте [gzrewind()](function.gzrewind.md), щоб перемістити вказівник на позицію на початок файлу, якщо ви вже записували дані до нього.

**Підказка**

Якщо потрібно просто вивести вміст файлу без переміщення вказівника на позицію або внесення змін, використовуйте функцію [readgzfile()](function.readgzfile.md), яка не вимагає виклику функції [gzopen()](function.gzopen.md)

### Список параметрів

`stream`

Вказівник на gz-файл, повернутий після його успішного відкриття функцією [gzopen()](function.gzopen.md)

### Значення, що повертаються

Кількість стиснутих символів, прочитаних з `gz` та переданих на вхід, або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **gzpassthru()****

```php
<?php
$fp = gzopen('file.gz', 'r');
gzpassthru($fp);
gzclose($fp);
?>
```
