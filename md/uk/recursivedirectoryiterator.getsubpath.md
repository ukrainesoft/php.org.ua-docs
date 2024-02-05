---
navigation:
  - recursivedirectoryiterator.getchildren.md: '« RecursiveDirectoryIterator::getChildren'
  - recursivedirectoryiterator.getsubpathname.md: 'RecursiveDirectoryIterator::getSubPathname »'
  - index.md: PHP Manual
  - class.recursivedirectoryiterator.md: RecursiveDirectoryIterator
title: 'RecursiveDirectoryIterator::getSubPath'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RecursiveDirectoryIterator::getSubPath

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

RecursiveDirectoryIterator::getSubPath — Повертає шлях до піддиректорії

### Опис

```methodsynopsis
public RecursiveDirectoryIterator::getSubPath(): string
```

Повертає шлях до піддиректорії щодо директорії, заданої у конструкторі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Шлях до піддиректорії.

### Приклади

**Пример #1 Пример использования**getSubPath()\*\*\*\*

```php
$directory = '/tmp';

      $it = new RecursiveIteratorIterator(new RecursiveDirectoryIterator($directory));

      foreach ($it as $file) {
          echo 'Имя файла: ' . $it->getSubPathName() . "\n";
          echo 'Поддиректория: ' . $it->getSubPath() . "\n\n";
      }
```

Висновок наведеного прикладу буде схожим на:

```
Имя файла: fruit/apple.xml
     Поддиректория: fruit

     Имя файла: stuff.xml
     Поддиректория:

     Имя файла: veggies/carrot.xml
     Поддиректория: veggies
```

### Дивіться також

-   [RecursiveDirectoryIterator::getSubPathName()](recursivedirectoryiterator.getsubpathname.md) \- Повертає шлях до піддиректорії та ім'я файлу
-   [RecursiveDirectoryIterator::key()](recursivedirectoryiterator.key.md) \- Повертає шлях та ім'я файлу поточного елемента
