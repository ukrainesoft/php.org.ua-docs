---
navigation:
  - class.directoryiterator.md: « DirectoryIterator
  - directoryiterator.current.md: 'DirectoryIterator::current »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DirectoryIterator::\_\_construct

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::\_\_construct — Створює новий ітератор каталогів зі шляху

### Опис

public**DirectoryIterator::\_\_construct**(string`$directory`) .

Створює новий ітератор каталогів із шляху.

### Список параметрів

`directory`

Шлях до каталогу, який потрібно обійти.

### Помилки

Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.md), якщо `directory` не існує.

Викидає помилку [ValueError](class.valueerror.md), якщо `directory` є порожнім рядком.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер викидається помилка [ValueError](class.valueerror.md), якщо `directory` є порожнім рядком; раніше викидався виняток [RuntimeException](class.runtimeexception.md) |

### Приклади

**Пример #1 Пример использования**DirectoryIterator::\_\_construct()\*\*\*\*

У цьому прикладі буде виведено вміст каталогу, що містить скрипт.

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
