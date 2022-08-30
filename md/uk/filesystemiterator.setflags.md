Завдання прапорів обробки

-   [« FilesystemIterator::rewind](filesystemiterator.rewind.md)
    
-   [FilterIterator »](class.filteriterator.md)
    
-   [PHP Manual](index.md)
    
-   [FilesystemIterator](class.filesystemiterator.md)
    
-   Завдання прапорів обробки
    

# FilesystemIterator::setFlags

(PHP 5> = 5.3.0, PHP 7, PHP 8)

FilesystemIterator::setFlags — Завдання прапорів обробки

### Опис

```methodsynopsis
public FilesystemIterator::setFlags(int $flags): void
```

Задає налаштування ітератора.

### Список параметрів

`flags`

Прапори, які потрібно встановити. Дивіться [Константи FilesystemIterator](class.filesystemiterator.html#filesystemiterator.constants)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання [FilesystemIterator::key()](filesystemiterator.key.md)**

Приклад демонструє різницю між прапорами [FilesystemIterator::KEYАСPATHNAME](class.filesystemiterator.html#filesystemiterator.constants.key-as-pathname) і [FilesystemIterator::KEYАСFILENAME](class.filesystemiterator.html#filesystemiterator.constants.key-as-filename)

```php
<?php
$iterator = new FilesystemIterator(dirname(__FILE__), FilesystemIterator::KEY_AS_PATHNAME);
echo "Ключом является путь к файлу:\n";
foreach ($iterator as $key => $fileinfo) {
    echo $key . "\n";
}

$iterator->setFlags(FilesystemIterator::KEY_AS_FILENAME);
echo "\nКлючом является имя файла:\n";
foreach ($iterator as $key => $fileinfo) {
    echo $key . "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ключом является путь к файлу:
/www/examples/apple.jpg
/www/examples/banana.jpg
/www/examples/example.php

Ключом является имя файла:
apple.jpg
banana.jpg
example.php
```

### Дивіться також

-   [FilesystemIterator::construct()](filesystemiterator.construct.md) - Створює новий ітератор файлової системи
-   [FilesystemIterator::getFlags()](filesystemiterator.getflags.md) - Отримання прапорів налаштувань об'єкта