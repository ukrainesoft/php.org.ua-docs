Повертає ім'я файлу (без розширення) поточного елемента DirectoryIterator

-   [« DirectoryIterator::getATime](directoryiterator.getatime.html)
    
-   [DirectoryIterator::getCTime »](directoryiterator.getctime.html)
    
-   [PHP Manual](index.html)
    
-   [DirectoryIterator](class.directoryiterator.html)
    
-   Повертає ім'я файлу (без розширення) поточного елемента DirectoryIterator
    

# DirectoryIterator::getBasename

(PHP 5> = 5.2.2, PHP 7, PHP 8)

DirectoryIterator::getBasename — Повертає ім'я файлу (без розширення) поточного елемента DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::getBasename(string $suffix = ""): string
```

Повертає ім'я файлу (без розширення) поточного елемента [DirectoryIterator](class.directoryiterator.html)

### Список параметрів

`suffix`

Якщо ім'я файлу закінчується на `suffix`, то він буде відкинутий.

### Значення, що повертаються

Ім'я файлу поточного елемента [DirectoryIterator](class.directoryiterator.html)

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::getBasename()****

Приклад виведе список імен файлів директорії, що містить скрипт. Якщо ім'я файлу закінчується на `.jpg`, цей суфікс буде відкинуто.

```php
<?php
$dir = new DirectoryIterator(dirname(__FILE__));
foreach ($dir as $fileinfo) {
    if ($fileinfo->isFile()) {
        echo $fileinfo->getBasename() . "\n";
        echo $fileinfo->getBasename('.jpg') . "\n";
    }
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
apple.jpg
apple
banana.jpg
banana
index.php
index.php
pear.jpg
pear
```

### Дивіться також

-   [DirectoryIterator::getFilename()](directoryiterator.getfilename.html) - Повертає ім'я файлу поточного елемента DirectoryIterator
-   [DirectoryIterator::getPath()](directoryiterator.getpath.html) - Повертає шлях до поточного елементу DirectoryIterator без імені файлу
-   [DirectoryIterator::getPathname()](directoryiterator.getpathname.html) - Повертає шлях та ім'я файлу поточного елемента DirectoryIterator
-   [basename()](function.basename.html) - Повертає останній компонент імені із зазначеного шляху
-   [pathinfo()](function.pathinfo.html) - Повертає інформацію про шлях до файлу