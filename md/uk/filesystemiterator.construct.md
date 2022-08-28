Створює новий ітератор файлової системи

-   [« FilesystemIterator](class.filesystemiterator.html)
    
-   [FilesystemIterator::current »](filesystemiterator.current.html)
    
-   [PHP Manual](index.html)
    
-   [FilesystemIterator](class.filesystemiterator.html)
    
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

Поведінку деяких методів можна встановити за допомогою прапорів. Список цих прапорів можна знайти на сторінці [предопределённых констант FilesystemIterator](class.filesystemiterator.html#filesystemiterator.constants). Також їх можна задати пізніше методом [FilesystemIterator::setFlags()](filesystemiterator.setflags.html)

> **Зауваження**
> 
> **`FilesystemIterator::SKIP_DOTS`** завжди встановлений і не може бути вилучений.

### Помилки

Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.html), якщо директорія `directory` не існує.

Викидає виняток [ValueError](class.valueerror.html), якщо параметр `directory` містить порожній рядок.

### список змін

| Версия | Описание                                                                                                                                                                              |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Тепер викидає виняток [ValueError](class.valueerror.html), якщо параметр `directory` містить порожній рядок; раніше викидався виняток [RuntimeException](class.runtimeexception.html) |

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

-   [FilesystemIterator::setFlags()](filesystemiterator.setflags.html) - Завдання прапорів обробки
-   [DirectoryIterator::\_\_construct()](directoryiterator.construct.html) - Створює новий ітератор директорій шляхом