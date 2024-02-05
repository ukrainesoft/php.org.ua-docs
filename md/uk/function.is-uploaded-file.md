---
navigation:
  - function.is-readable.md: « is\_readable
  - function.is-writable.md: is\_writable »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: is\_uploaded\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_uploaded\_file

(PHP 4 >= 4.0.3, PHP 5, PHP 7, PHP 8)

is\_uploaded\_file — Визначає, чи завантажено файл за допомогою HTTP POST

### Опис

```methodsynopsis
is_uploaded_file(string $filename): bool
```

Повертає **`true`**, якщо файл `filename` був завантажений за допомогою HTTP POST. Це корисно для засвідчення того, що зловмисний користувач не намагається обдурити скрипт так, щоб він працював із файлами, з якими працювати не повинен – наприклад, /etc/passwd.

Такі перевірки особливо корисні, якщо існує можливість, що операції над файлом можуть показати його вміст користувачеві або навіть іншим користувачам тієї ж системи.

Для правильної роботи функції \*\*is\_uploaded\_file()\*\*нужен аргумент вида[$\_FILES\['userfile'\]\['tmp\_name'\]](reserved.variables.files.md), - имя загруженного файла на клиентской машине[$\_FILES\['userfile'\]\['name'\]](reserved.variables.files.md)не подходит.

### Список параметрів

`filename`

Ім'я файлу, що перевіряється.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання функції** is\_uploaded\_file()\*\*\*\*

```php
<?php

if (is_uploaded_file($_FILES['userfile']['tmp_name'])) {
   echo "Файл ". $_FILES['userfile']['name'] ." успешно загружен.\n";
   echo "Отображаем содержимое\n";
   readfile($_FILES['userfile']['tmp_name']);
} else {
   echo "Возможная атака с участием загрузки файла: ";
   echo "файл '". $_FILES['userfile']['tmp_name'] . "'.";
}

?>
```

### Дивіться також

-   [move\_uploaded\_file()](function.move-uploaded-file.md) \- Переміщує завантажений файл у нове місце
-   [$\_FILES](reserved.variables.files.md)
-   Простий приклад використання можна знайти у розділі "[Завантаження файлів на сервер](features.file-upload.md)".
