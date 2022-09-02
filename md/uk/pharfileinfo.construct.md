---
navigation:
  - pharfileinfo.compress.md: '« PharFileInfo::compress'
  - pharfileinfo.decompress.md: 'PharFileInfo::decompress »'
  - index.md: PHP Manual
  - class.pharfileinfo.md: PharFileInfo
title: 'PharFileInfo::construct'
---
# PharFileInfo::construct

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

PharFileInfo::construct — Конструктор об'єкта PharFileInfo

### Опис

public **PharFileInfo::construct**(string `$filename`

Не повинен викликатись безпосередньо. Об'єкт PharFileInfo слід ініціалізувати за допомогою [Phar::offsetGet()](phar.offsetget.md)за допомогою синтаксису доступу до масиву.

### Список параметрів

`filename`

Повний URL-файл. Якщо ви хочете вийняти файл `my/file.php` з архіву `boo.phar`необхідно задати `phar://boo.phar/my/file.php`

### Помилки

Викидає виняток [BadMethodCallException](class.badmethodcallexception.md), якщо [construct()](language.oop5.decon.md#object.construct) викликаний двічі. Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.md), якщо запитаний URL некоректний, phar-архів неможливо відкрити або якщо вказаний файл відсутній в архіві.

### Приклади

**Приклад #1 Приклад використання **PharFileInfo::construct()****

```php
<?php
try {
    $p = new Phar('/path/to/my.phar', 0, 'my.phar');
    $p['testfile.txt'] = "hi\nthere\ndude";
    $file = $p['testfile.txt'];
    foreach ($file as $line => $text) {
        echo "номер строки $line: $text";
    }
    // так то же работает
    $file = new PharFileInfo('phar:///path/to/my.phar/testfile.txt');
    foreach ($file as $line => $text) {
        echo "номер строки $line: $text";
    }
} catch (Exception $e) {
    echo 'Операции Phar завершились ошибкой;
}
?>
```

Результат виконання цього прикладу:

```
номер строки 1: hi
номер строки 2: there
номер строки 3: dude
номер строки 1: hi
номер строки 2: there
номер строки 3: dude
```
