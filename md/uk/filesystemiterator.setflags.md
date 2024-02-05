---
navigation:
  - filesystemiterator.rewind.md: '« FilesystemIterator::rewind'
  - class.filteriterator.md: FilterIterator »
  - index.md: PHP Manual
  - class.filesystemiterator.md: FilesystemIterator
title: 'FilesystemIterator::setFlags'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# FilesystemIterator::setFlags

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

FilesystemIterator::setFlags — Завдання прапорів обробки

### Опис

```methodsynopsis
public FilesystemIterator::setFlags(int $flags): void
```

Задає налаштування ітератора.

### Список параметрів

`flags`

Прапори, які потрібно встановити. Дивіться [Константи FilesystemIterator](class.filesystemiterator.md#filesystemiterator.constants)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования[FilesystemIterator::key()](filesystemiterator.key.md)**

Приклад демонструє різницю між прапорами [FilesystemIterator::KEY\_AS\_PATHNAME](class.filesystemiterator.md#filesystemiterator.constants.key-as-pathname) і [FilesystemIterator::KEY\_AS\_FILENAME](class.filesystemiterator.md#filesystemiterator.constants.key-as-filename)

```php
<?php
$iterator = new FilesystemIterator(dirname(__FILE__), FilesystemIterator::KEY_AS_PATHNAME);
echo "Ключом является путь к файлу:\n";
foreach ($iterator as $key => $fileinfo) {
    echo $key . "\n";
}

$iterator->setFlags(FilesystemIterator::KEY_AS_FILENAME);
echo "\nКлючом является имя файла:\n";
foreach ($iterator as $key => $fileinfo) {
    echo $key . "\n";
}
?>
```

Результат виконання наведеного прикладу PHP 8.2 аналогічний:

```
Ключом является путь к файлу:
/www/examples/.
/www/examples/..
/www/examples/apple.jpg
/www/examples/banana.jpg
/www/examples/example.php

Ключом является имя файла:
.
..
apple.jpg
banana.jpg
example.php
```

### Дивіться також

-   [FilesystemIterator::\_\_construct()](filesystemiterator.construct.md) \- Створює новий ітератор файлової системи
-   [FilesystemIterator::getFlags()](filesystemiterator.getflags.md) \- Отримання прапорів налаштувань об'єкта
