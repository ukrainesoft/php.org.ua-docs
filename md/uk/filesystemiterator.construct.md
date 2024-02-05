---
navigation:
  - class.filesystemiterator.md: « FilesystemIterator
  - filesystemiterator.current.md: 'FilesystemIterator::current »'
  - index.md: PHP Manual
  - class.filesystemiterator.md: FilesystemIterator
title: 'FilesystemIterator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# FilesystemIterator::\_\_construct

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

FilesystemIterator::\_\_construct — Створює новий ітератор файлової системи

### Опис

public**FilesystemIterator::\_\_construct**(string`$directory`, int`$flags`\= FilesystemIterator::KEY\_AS\_PATHNAME | FilesystemIterator::CURRENT\_AS\_FILEINFO | FilesystemIterator::SKIP\_DOTS)

Створює новий об'єкт ітератора файлової системи на основі аргументу `directory`

### Список параметрів

`directory`

Шлях до об'єкта файлової системи яким потрібно навігація.

`flags`

Поведінку деяких методів можна встановити за допомогою прапорів. Список цих прапорів можна знайти на сторінці [визначених констант FilesystemIterator](class.filesystemiterator.md#filesystemiterator.constants). Також їх можна задати пізніше методом [FilesystemIterator::setFlags()](filesystemiterator.setflags.md)

### Помилки

Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.md), якщо директорія `directory` не існує.

Викидає виняток [ValueError](class.valueerror.md), якщо параметр `directory` містить порожній рядок.

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | До версії PHP 8.2.0, константа **`FilesystemIterator::SKIP_DOTS`** завжди була встановлена ​​і не могла бути видалена. |
| 8.0.0 | Тепер викидає виняток [ValueError](class.valueerror.md), якщо параметр `directory` містить порожній рядок; раніше викидався виняток [RuntimeException](class.runtimeexception.md) |

### Приклади

**Пример #1 Пример использования**FilesystemIterator::\_\_construct()\*\*\*\*

```php
<?php
$it = new FilesystemIterator(dirname(__FILE__), FilesystemIterator::CURRENT_AS_FILEINFO);
foreach ($it as $fileinfo) {
    echo $fileinfo->getFilename() . "\n";
}
?>
```

Результат виконання наведеного прикладу PHP 8.2 аналогічний:

```
.
..
apples.jpg
banana.jpg
example.php
```

Висновок наведеного вище прикладу до версії PHP 8.2.0 виглядає так:

```
apples.jpg
banana.jpg
example.php
```

### Дивіться також

-   [FilesystemIterator::setFlags()](filesystemiterator.setflags.md) \- Завдання прапорів обробки
-   [DirectoryIterator::\_\_construct()](directoryiterator.construct.md) \- Створює новий ітератор каталогів зі шляху
