---
navigation:
  - phar.hasmetadata.html: '« Phar::hasMetadata'
  - phar.isbuffering.html: 'Phar::isBuffering »'
  - index.html: PHP Manual
  - class.phar.html: Phar
title: 'Phar::interceptFileFuncs'
---
# Phar::interceptFileFuncs

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::interceptFileFuncs — Вказує phar перехоплювати fopen, filegetcontents, opendir та всі stat-функції

### Опис

```methodsynopsis
final public static Phar::interceptFileFuncs(): void
```

Вказує phar перехоплювати [fopen()](function.fopen.html) [readfile()](function.readfile.html) [filegetcontents()](function.file-get-contents.html) [opendir()](function.opendir.md) та всі stat-функції. Якщо будь-яка з цих функцій буде викликана з phar-архіву з відносним шляхом, виклик буде модифіковано для доступу до вмісту архіву. У випадку з абсолютними шляхами працюватимуть штатні функції доступу до файлової системи.

Ця функція дозволяє писати програми, які працюють не прив'язані до жорсткого диска.

### Список параметрів

No parameters.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **Phar::interceptFileFuncs()****

```php
<?php
Phar::interceptFileFuncs();
include 'phar://' . __FILE__ . '/file.php';
?>
```

Припустимо, що ми маємо `/path/to/myphar.phar` і в ньому містяться файли `file.php` і `file2.txt`. . `file.php` містить такий код:

**Приклад #2 Приклад використання **Phar::interceptFileFuncs()****

```php
<?php
echo file_get_contents('file2.txt');
?>
```

У звичайному режимі PHP шукатиме `file2.txt` у поточній директорії, що є директорією запуску file.php, або поточною директорією у разі використання командного рядка . **Phar::interceptFileFuncs()** вкаже PHP, що поточна директорія - це `phar:///path/to/myphar.phar/` і, наприклад, буде відкритий файл `phar:///path/to/myphar.phar/file2.txt`
