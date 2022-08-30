Повертає ім'я файлу у вигляді рядка

-   [« DirectoryIterator::seek](directoryiterator.seek.html)
    
-   [DirectoryIterator::valid »](directoryiterator.valid.html)
    
-   [PHP Manual](index.html)
    
-   [DirectoryIterator](class.directoryiterator.html)
    
-   Повертає ім'я файлу у вигляді рядка
    

# DirectoryIterator::toString

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::toString — Повертає ім'я файлу у вигляді рядка

### Опис

```methodsynopsis
public
   DirectoryIterator::__toString(): string
```

Повертає ім'я файлу поточного елемента [DirectoryIterator](class.directoryiterator.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я файлу поточного елемента [DirectoryIterator](class.directoryiterator.html)

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::toString()****

Приклад виведе список вмісту директорії, що містить скрипт.

```php
<?php
$dir = new DirectoryIterator(dirname(__FILE__));
foreach ($dir as $fileinfo) {
    echo $fileinfo;
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
.
..
apple.jpg
banana.jpg
index.php
pear.jpg
```

### Дивіться також

-   [DirectoryIterator::getFilename()](directoryiterator.getfilename.html) - Повертає ім'я файлу поточного елемента DirectoryIterator
-   Магічний метод [toString()](language.oop5.magic.html#object.tostring)