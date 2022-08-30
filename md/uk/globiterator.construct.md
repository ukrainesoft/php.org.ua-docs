Створює ітератор директорії, використовуючи glob-вираз

-   [« GlobIterator](class.globiterator.html)
    
-   [GlobIterator::count »](globiterator.count.html)
    
-   [PHP Manual](index.html)
    
-   [GlobIterator](class.globiterator.html)
    
-   Створює ітератор директорії, використовуючи glob-вираз
    

# GlobIterator::construct

(PHP 5> = 5.3.0, PHP 7, PHP 8)

GlobIterator::construct - Створює ітератор директорії, використовуючи glob-вираз

### Опис

public **GlobIterator::construct**(string `$pattern`, int `$flags` = FilesystemIterator::KEYАСPATHNAME | FilesystemIterator::CURRENTАСFILEINFO)

Створює новий ітератор директорії на основі glob-виразу.

### Список параметрів

`pattern`

Шаблон [glob()](function.glob.html)

`flags`

Прапори налаштування. Прапори можна ставити бітовою маскою констант [FilesystemIterator](class.filesystemiterator.html)

### Помилки

Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.html), якщо директорія `directory` не існує.

Викидає виняток [ValueError](class.valueerror.html), якщо параметр `directory` містить порожній рядок.

### список змін

| Версия | Описание                                                                                                                                                                              |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Тепер викидає виняток [ValueError](class.valueerror.html), якщо параметр `directory` містить порожній рядок. Раніше викидався виняток [RuntimeException](class.runtimeexception.html) |

### Приклади

**Приклад #1 Приклад використання [GlobIterator](class.globiterator.html)**

```php
<?php
$iterator = new GlobIterator('*.dll', FilesystemIterator::KEY_AS_FILENAME);

if (!$iterator->count()) {
    echo 'Нет совпадений';
} else {
    $n = 0;

    printf("Найдено элементов: %d \r\n", $iterator->count());

    foreach ($iterator as $item) {
        printf("[%d] %s\r\n", ++$n, $iterator->key());
    }
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Найдено элементов: 2
[1] php5ts.dll
[2] php_gd2.dll
```

### Дивіться також

-   [DirectoryIterator::construct()](directoryiterator.construct.html) - Створює новий ітератор директорій шляхом
-   [GlobIterator::count()](globiterator.count.html) - Визначає кількість директорій та файлів
-   [glob()](function.glob.html) - Знаходить файлові шляхи, що збігаються із шаблоном