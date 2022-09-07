---
navigation:
  - class.directoryiterator.md: « DirectoryIterator
  - directoryiterator.current.md: 'DirectoryIterator::current »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
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

Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.md) у разі, якщо директорія `directory` не існує.

Викидає виняток [ValueError](class.valueerror.md), якщо параметр `directory` містить порожній рядок.

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер викидає виняток [ValueError](class.valueerror.md), якщо параметр `directory` містить порожній рядок; раніше викидався виняток [RuntimeException](class.runtimeexception.md) |

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::construct()****

Приклад виведе список вмісту директорії, що містить скрипт, що виконується.

```php
<?php
$dir = new DirectoryIterator(dirname(__FILE__));
foreach ($dir as $fileinfo) {
    if (!$fileinfo->isDot()) {
        var_dump($fileinfo->getFilename());
    }
}
?>
```

### Дивіться також

-   [SplFileInfo](class.splfileinfo.md)
-   [Iterator](class.iterator.md)
