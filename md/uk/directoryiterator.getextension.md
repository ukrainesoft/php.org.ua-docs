---
navigation:
  - directoryiterator.getbasename.md: '« DirectoryIterator::getBasename'
  - directoryiterator.getfilename.md: 'DirectoryIterator::getFilename »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::getExtension'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DirectoryIterator::getExtension

(PHP 5 >= 5.3.6, PHP 7, PHP 8)

DirectoryIterator::getExtension — Отримує розширення файлу

### Опис

```methodsynopsis
public DirectoryIterator::getExtension(): string
```

Отримує розширення файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок (string), що містить розширення файлу або порожній рядок (string), якщо файл не має розширення.

### Приклади

**Приклад #1 Приклад використання** DirectoryIterator::getExtension()\*\*\*\*

```php
<?php

$directory = new DirectoryIterator(__DIR__);
foreach ($directory as $fileinfo) {
    if ($fileinfo->isFile()) {
        echo $fileinfo->getExtension() . "\n";
    }
}

?>
```

Висновок наведеного прикладу буде схожим на:

```
php
txt
jpg
gz
```

### Примітки

> **Зауваження** :
> 
> Іншим способом отримання розширення є використання функції [pathinfo()](function.pathinfo.md)
> 
> ```php
> <?php
> $extension = pathinfo($fileinfo->getFilename(), PATHINFO_EXTENSION);
> ?>
> ```

### Дивіться також

-   [DirectoryIterator::getFilename()](directoryiterator.getfilename.md) \- Повертає ім'я файлу поточного елемента DirectoryIterator
-   [DirectoryIterator::getBasename()](directoryiterator.getbasename.md) \- Отримує базове ім'я поточного елемента DirectoryIterator
-   [pathinfo()](function.pathinfo.md) \- Повертає інформацію про шлях до файлу
