---
navigation:
  - directoryiterator.getfilename.md: '« DirectoryIterator::getFilename'
  - directoryiterator.key.md: 'DirectoryIterator::key »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::isDot'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DirectoryIterator::isDot

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::isDot — Визначає, чи є поточний елемент DirectoryIterator '.' або '.'.

### Опис

```methodsynopsis
public DirectoryIterator::isDot(): bool
```

Визначає, чи є поточний елемент [DirectoryIterator](class.directoryiterator.md) или `.. .`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо елемент є или `.. .` , в іншому випадку повертає **`false`**

### Приклади

**Пример #1 Пример использования**DirectoryIterator::isDot()\*\*\*\*

У цьому прикладі будуть перераховані всі файли, за винятком елементів и `.. .`

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if (!$fileinfo->isDot()) {
        echo $fileinfo->getFilename() . "\n";
    }
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
apple.jpg
banana.jpg
example.php
pears.jpg
```

### Дивіться також

-   **DirectoryIterator::getType()**
-   **DirectoryIterator::isDir()**
-   **DirectoryIterator::isFile()**
-   **DirectoryIterator::isLink()**
