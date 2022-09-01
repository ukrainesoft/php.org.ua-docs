---
navigation:
  - class.directoryiterator.html: « DirectoryIterator
  - directoryiterator.current.html: 'DirectoryIterator::current »'
  - index.html: PHP Manual
  - class.directoryiterator.html: DirectoryIterator
title: 'DirectoryIterator::construct'
---
# DirectoryIterator::construct

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::construct — Створює новий ітератор директорій на шляху

### Опис

public **DirectoryIterator::construct**(string `$directory`

Створює новий ітератор директорій на шляху.

### Список параметрів

`directory`

Дорога до директорії для проходу.

### Помилки

Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.html) у разі, якщо директорія `directory` не існує.

Викидає виняток [ValueError](class.valueerror.html), якщо параметр `directory` містить порожній рядок.

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер викидає виняток [ValueError](class.valueerror.html), якщо параметр `directory` містить порожній рядок; раніше викидався виняток [RuntimeException](class.runtimeexception.html) |

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::construct()****

Приклад виведе список вмісту директорії, що містить скрипт, що виконується.

```php
<?php
$dir = new DirectoryIterator(dirname(__FILE__));
foreach ($dir as $fileinfo) {
    if (!$fileinfo->isDot()) {
        var_dump($fileinfo->getFilename());
    }
}
?>
```

### Дивіться також

-   [SplFileInfo](class.splfileinfo.html)
-   [Iterator](class.iterator.html)
