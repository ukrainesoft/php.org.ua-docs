Визначає, чи файл завантажений за допомогою HTTP POST

-   [« is\_readable](function.is-readable.html)
    
-   [is\_writable »](function.is-writable.html)
    
-   [PHP Manual](index.html)
    
-   [Функции файловой системы](ref.filesystem.html)
    
-   Визначає, чи файл завантажений за допомогою HTTP POST
    

# ісuploadedfile

(PHP 4> = 4.0.3, PHP 5, PHP 7, PHP 8)

ісuploadedfile — Визначає, чи завантажено файл за допомогою HTTP POST

### Опис

```methodsynopsis
is_uploaded_file(string $filename): bool
```

Повертає **`true`**, якщо файл `filename` був завантажений за допомогою HTTP POST. Це корисно для посвідчення того, що зловмисний користувач не намагається обдурити скрипт так, щоб він працював із файлами, з якими працювати не повинен – наприклад, /etc/passwd.

Такі перевірки особливо корисні, якщо існує можливість, що операції над файлом можуть показати його вміст користувачеві або навіть іншим користувачам тієї ж системи.

Для правильної роботи функції **ісuploadedfile()** потрібен аргумент виду [$\_FILES\['userfile'\]\['tmp\_name'\]](reserved.variables.files.html), - ім'я завантаженого файлу на клієнтській машині [$\_FILES\['userfile'\]\['name'\]](reserved.variables.files.html) не підходить.

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

-   [move\_uploaded\_file()](function.move-uploaded-file.html) - Переміщує завантажений файл у нове місце
-   [$\_FILES](reserved.variables.files.html)
-   Простий приклад використання можна знайти у розділі "[Загрузка файлов на сервер](features.file-upload.html)".