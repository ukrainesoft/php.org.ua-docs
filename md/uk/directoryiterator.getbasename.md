---
navigation:
  - directoryiterator.current.md: '« DirectoryIterator::current'
  - directoryiterator.getextension.md: 'DirectoryIterator::getExtension »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::getBasename'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DirectoryIterator::getBasename

(PHP 5 >= 5.2.2, PHP 7, PHP 8)

DirectoryIterator::getBasename — Отримує базове ім'я поточного елемента DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::getBasename(string $suffix = ""): string
```

Отримує базове ім'я поточного елемента [DirectoryIterator](class.directoryiterator.md)

### Список параметрів

`suffix`

Якщо базове ім'я закінчується на `suffix`, то він буде відкинутий.

### Значення, що повертаються

Базове ім'я поточного елемента [DirectoryIterator](class.directoryiterator.md)

### Приклади

**Приклад #1 Приклад використання** DirectoryIterator::getBasename()\*\*\*\*

У цьому прикладі для файлів у каталозі, що містить скрипт, буде перераховано повне базове ім'я та базове ім'я з віддаленим суфіксом `.jpg`

```php
<?php
$dir = new DirectoryIterator(dirname(__FILE__));
foreach ($dir as $fileinfo) {
    if ($fileinfo->isFile()) {
        echo $fileinfo->getBasename() . "\n";
        echo $fileinfo->getBasename('.jpg') . "\n";
    }
}
?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [DirectoryIterator::getFilename()](directoryiterator.getfilename.md) \- Повертає ім'я файлу поточного елемента DirectoryIterator
-   **DirectoryIterator::getPath()**
-   **DirectoryIterator::getPathname()**
-   [basename()](function.basename.md) \- Повертає останній компонент імені із зазначеного шляху
-   [pathinfo()](function.pathinfo.md) \- Повертає інформацію про шлях до файлу
