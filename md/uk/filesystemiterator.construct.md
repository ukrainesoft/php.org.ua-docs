Створює новий ітератор файлової системи

-   [« FilesystemIterator](class.filesystemiterator.md)
    
-   [FilesystemIterator::current »](filesystemiterator.current.md)
    
-   [PHP Manual](index.md)
    
-   [FilesystemIterator](class.filesystemiterator.md)
    
-   Створює новий ітератор файлової системи
    

# FilesystemIterator::construct

(PHP 5> = 5.3.0, PHP 7, PHP 8)

FilesystemIterator::construct — Створює новий ітератор файлової системи

### Опис

public **FilesystemIterator::construct**(string `$directory`, int `$flags` = FilesystemIterator::KEYАСPATHNAME | FilesystemIterator::CURRENTАСFILEINFO | FilesystemIterator::SKIPDOTS)

Створює новий об'єкт ітератора файлової системи на основі аргументу `directory`

### Список параметрів

`directory`

Шлях до об'єкта файлової системи яким потрібно навігація.

`flags`

Поведінку деяких методів можна встановити за допомогою прапорів. Список цих прапорів можна знайти на сторінці [визначених констант FilesystemIterator](class.filesystemiterator.html#filesystemiterator.constants). Також їх можна задати пізніше методом [FilesystemIterator::setFlags()](filesystemiterator.setflags.md)

> **Зауваження**
> 
> **`FilesystemIterator::SKIP_DOTS`** завжди встановлений і не може бути вилучений.

### Помилки

Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.md), якщо директорія `directory` не існує.

Викидає виняток [ValueError](class.valueerror.md), якщо параметр `directory` містить порожній рядок.

### список змін

| Версия | Описание                                                                                                                                                                          |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Тепер викидає виняток [ValueError](class.valueerror.md), якщо параметр `directory` містить порожній рядок; раніше викидався виняток [RuntimeException](class.runtimeexception.md) |

### Приклади

**Приклад #1 Приклад використання **FilesystemIterator::construct()****

```php
<?php
$it = new FilesystemIterator(dirname(__FILE__));
foreach ($it as $fileinfo) {
    echo $fileinfo->getFilename() . "\n";
}
?>
```

Результат виконання цього прикладу:

```
apples.jpg
banana.jpg
example.php
```

### Дивіться також

-   [FilesystemIterator::setFlags()](filesystemiterator.setflags.md) - Завдання прапорів обробки
-   [DirectoryIterator::construct()](directoryiterator.construct.md) - Створює новий ітератор директорій шляхом