Повертає ключ поточного елемента DirectoryIterator

-   [« DirectoryIterator::isWritable](directoryiterator.iswritable.md)
    
-   [DirectoryIterator::next »](directoryiterator.next.md)
    
-   [PHP Manual](index.md)
    
-   [DirectoryIterator](class.directoryiterator.md)
    
-   Повертає ключ поточного елемента DirectoryIterator
    

# DirectoryIterator::key

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::key — Повертає ключ поточного елемента DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::key(): mixed
```

Повертає ключ поточного елемента [DirectoryIterator](class.directoryiterator.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ключ поточного елемента [DirectoryIterator](class.directoryiterator.md) як цілого числа (int).

### список змін

| Версия | Описание                                                                                                               |
|--------|------------------------------------------------------------------------------------------------------------------------|
|        | Якщо ітератор не ініціалізований, тепер викидається помилка [Error](class.error.md). Раніше метод повертав **`false`** |

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::key()****

```php
<?php
$dir = new DirectoryIterator(dirname(__FILE__));
foreach ($dir as $fileinfo) {
    if (!$fileinfo->isDot()) {
        echo $fileinfo->key() . " => " . $fileinfo->getFilename() . "\n";
    }
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
0 => apple.jpg
1 => banana.jpg
2 => index.php
3 => pear.jpg
```

### Дивіться також

-   [DirectoryIterator::current()](directoryiterator.current.md) - Повертає поточний елемент DirectoryIterator
-   [DirectoryIterator::next()](directoryiterator.next.md) - Переміщує покажчик на наступний елемент DirectoryIterator
-   [DirectoryIterator::rewind()](directoryiterator.rewind.md) - Встановлює покажчик на перший елемент DirectoryIterator
-   [DirectoryIterator::valid()](directoryiterator.valid.md) - Перевіряє, чи є поточний елемент DirectoryIterator допустимим файлом
-   [Iterator::key()](iterator.key.md) - Повертає ключ поточного елемента