---
navigation:
  - class.recursivedirectoryiterator.md: « RecursiveDirectoryIterator
  - recursivedirectoryiterator.getchildren.md: 'RecursiveDirectoryIterator::getChildren »'
  - index.md: PHP Manual
  - class.recursivedirectoryiterator.md: RecursiveDirectoryIterator
title: 'RecursiveDirectoryIterator::construct'
---
# RecursiveDirectoryIterator::construct

(PHP 5> = 5.1.2, PHP 7, PHP 8)

RecursiveDirectoryIterator::construct — Конструктор класу RecursiveDirectoryIterator

### Опис

public **RecursiveDirectoryIterator::construct**(string `$directory`, int `$flags` = FilesystemIterator::KEYАСPATHNAME | FilesystemIterator::CURRENTАСFILEINFO)

Створює новий об'єкт класу **RecursiveDirectoryIterator()**, використовуючи заданий шлях `directory`

### Список параметрів

`directory`

Шлях до директорії, якою здійснюватиметься навігація.

`flags`

Можна встановити кілька прапорів, від яких залежатиме поведінка деяких методів. Список можливих прапорів можна знайти на сторінці [Обумовлених констант класу FilesystemIterator](class.filesystemiterator.md#filesystemiterator.constants). Прапори можна задати пізніше методом [FilesystemIterator::setFlags()](filesystemiterator.setflags.md)

### Помилки

Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.md), якщо директорія `directory` не існує.

Викидає виняток [ValueError](class.valueerror.md), якщо параметр `directory` містить порожній рядок.

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер викидає виняток [ValueError](class.valueerror.md), якщо параметр `directory` містить порожній рядок. раніше викидався виняток [RuntimeException](class.runtimeexception.md) |

### Приклади

**Приклад #1 Приклад використання [RecursiveDirectoryIterator](class.recursivedirectoryiterator.md)**

```php
<?php

$directory = '/tmp';

$it = new RecursiveIteratorIterator(new RecursiveDirectoryIterator($directory));

$it->rewind();
while($it->valid()) {

    if (!$it->isDot()) {
        echo 'Имя файла: ' . $it->getSubPathName() . "\n";
        echo 'Поддиректория: ' . $it->getSubPath() . "\n";
        echo 'Ключ: ' . $it->key() . "\n\n";
    }

    $it->next();
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Имя файла: fruit/apple.xml
Поддиректория: fruit
Ключ: /tmp/fruit/apple.xml

Имя файла: stuff.xml
Поддиректория:
Ключ: /tmp/stuff.xml

Имя файла: veggies/carrot.xml
Поддиректория: veggies
Ключ: /tmp/veggies/carrot.xml
```

### Дивіться також

-   [FilesystemIterator::construct()](filesystemiterator.construct.md) - Створює новий ітератор файлової системи
-   [RecursiveIteratorIterator::construct()](recursiveiteratoriterator.construct.md) - Конструктор класу RecursiveIteratorIterator
-   [Обумовлені константи класса FilesystemIterator](class.filesystemiterator.md#filesystemiterator.constants)
