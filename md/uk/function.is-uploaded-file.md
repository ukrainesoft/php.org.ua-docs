---
navigation:
  - function.is-readable.html: « isreadable
  - function.is-writable.html: ісwritable »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: ісuploadedfile
---
# ісuploadedfile

(PHP 4> = 4.0.3, PHP 5, PHP 7, PHP 8)

ісuploadedfile — Визначає, чи завантажено файл за допомогою HTTP POST

### Опис

```methodsynopsis
is_uploaded_file(string $filename): bool
```

Повертає **`true`**, якщо файл `filename` був завантажений за допомогою HTTP POST. Це корисно для посвідчення того, що зловмисний користувач не намагається обдурити скрипт так, щоб він працював із файлами, з якими працювати не повинен – наприклад, /etc/passwd.

Такі перевірки особливо корисні, якщо існує можливість, що операції над файлом можуть показати його вміст користувачеві або навіть іншим користувачам тієї ж системи.

Для правильної роботи функції **ісuploadedfile()** потрібен аргумент виду [FILES\['userfile'\]\['tmpname'\]](reserved.variables.files.md), - ім'я завантаженого файлу на клієнтській машині [FILES\['userfile'\]\['name'\]](reserved.variables.files.md) не підходить.

### Список параметрів

`filename`

Ім'я файлу, що перевіряється.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання функції **ісuploadedfile()****

```php
<?php

if (is_uploaded_file($_FILES['userfile']['tmp_name'])) {
   echo "Файл ". $_FILES['userfile']['name'] ." успешно загружен.\n";
   echo "Отображаем содержимое\n";
   readfile($_FILES['userfile']['tmp_name']);
} else {
   echo "Возможная атака с участием загрузки файла: ";
   echo "файл '". $_FILES['userfile']['tmp_name'] . "'.";
}

?>
```

### Дивіться також

-   [moveuploadedfile()](function.move-uploaded-file.html) - Переміщує завантажений файл у нове місце
-   [FILES](reserved.variables.files.md)
-   Простий приклад використання можна знайти у розділі "[Загрузка файлов на сервер](features.file-upload.html)".
