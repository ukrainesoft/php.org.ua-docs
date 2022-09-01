---
navigation:
  - recursivedirectoryiterator.getsubpath.md: '« RecursiveDirectoryIterator::getSubPath'
  - recursivedirectoryiterator.haschildren.md: 'RecursiveDirectoryIterator::hasChildren »'
  - index.md: PHP Manual
  - class.recursivedirectoryiterator.md: RecursiveDirectoryIterator
title: 'RecursiveDirectoryIterator::getSubPathname'
---
# RecursiveDirectoryIterator::getSubPathname

(PHP 5> = 5.1.0, PHP 7, PHP 8)

RecursiveDirectoryIterator::getSubPathname — Повертає шлях до піддиректорії та ім'я файлу

### Опис

```methodsynopsis
public RecursiveDirectoryIterator::getSubPathname(): string
```

Повертає шлях до піддиректорії та ім'я файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає шлях до піддиректорії та ім'я файлу.

### Приклади

**Приклад #1 Приклад використання **getSubPathname()****

```php
$directory = '/tmp';

      $it = new RecursiveIteratorIterator(new RecursiveDirectoryIterator($directory));

      foreach ($it as $file) {
          echo 'Имя файла: ' . $it->getSubPathName() . "\n";
          echo 'Поддиректория: ' . $it->getSubPath() . "\n\n";
      }
```

Результатом виконання цього прикладу буде щось подібне:

```
Имя файла: fruit/apple.xml
     Поддиректория: fruit

     Имя файла: stuff.xml
     Поддиректория:

     Имя файла: veggies/carrot.xml
     Поддиректория: veggies
```

### Дивіться також

-   [RecursiveDirectoryIterator::getSubPath()](recursivedirectoryiterator.getsubpath.md) - Повертає шлях до піддиректорії
-   [RecursiveDirectoryIterator::key()](recursivedirectoryiterator.key.md) - Повертає шлях та ім'я файлу поточного елемента
