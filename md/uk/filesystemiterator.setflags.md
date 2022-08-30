Завдання прапорів обробки

-   [« FilesystemIterator::rewind](filesystemiterator.rewind.html)
    
-   [FilterIterator »](class.filteriterator.html)
    
-   [PHP Manual](index.html)
    
-   [FilesystemIterator](class.filesystemiterator.html)
    
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

Прапори, які потрібно встановити. Дивіться [Константы FilesystemIterator](class.filesystemiterator.html#filesystemiterator.constants)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання [FilesystemIterator::key()](filesystemiterator.key.html)**

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

-   [FilesystemIterator::construct()](filesystemiterator.construct.html) - Створює новий ітератор файлової системи
-   [FilesystemIterator::getFlags()](filesystemiterator.getflags.html) - Отримання прапорів налаштувань об'єкта