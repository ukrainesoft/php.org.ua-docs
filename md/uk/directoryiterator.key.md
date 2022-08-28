Повертає ключ поточного елемента DirectoryIterator

-   [« DirectoryIterator::isWritable](directoryiterator.iswritable.html)
    
-   [DirectoryIterator::next »](directoryiterator.next.html)
    
-   [PHP Manual](index.html)
    
-   [DirectoryIterator](class.directoryiterator.html)
    
-   Повертає ключ поточного елемента DirectoryIterator
    

# DirectoryIterator::key

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::key — Повертає ключ поточного елемента DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::key(): mixed
```

Повертає ключ поточного елемента [DirectoryIterator](class.directoryiterator.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ключ поточного елемента [DirectoryIterator](class.directoryiterator.html) як цілого числа (int).

### список змін

| Версия | Описание |
| --- | --- |
|  | Якщо ітератор не ініціалізований, тепер викидається помилка [Error](class.error.html). Раніше метод повертав **`false`** |

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

-   [DirectoryIterator::current()](directoryiterator.current.html) - Повертає поточний елемент DirectoryIterator
-   [DirectoryIterator::next()](directoryiterator.next.html) - Переміщує покажчик на наступний елемент DirectoryIterator
-   [DirectoryIterator::rewind()](directoryiterator.rewind.html) - Встановлює покажчик на перший елемент DirectoryIterator
-   [DirectoryIterator::valid()](directoryiterator.valid.html) - Перевіряє, чи є поточний елемент DirectoryIterator допустимим файлом
-   [Iterator::key()](iterator.key.html) - Повертає ключ поточного елемента