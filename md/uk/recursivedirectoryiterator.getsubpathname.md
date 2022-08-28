Повертає шлях до піддиректорії та ім'я файлу

-   [« RecursiveDirectoryIterator::getSubPath](recursivedirectoryiterator.getsubpath.html)
    
-   [RecursiveDirectoryIterator::hasChildren »](recursivedirectoryiterator.haschildren.html)
    
-   [PHP Manual](index.html)
    
-   [RecursiveDirectoryIterator](class.recursivedirectoryiterator.html)
    
-   Повертає шлях до піддиректорії та ім'я файлу
    

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

-   [RecursiveDirectoryIterator::getSubPath()](recursivedirectoryiterator.getsubpath.html) - Повертає шлях до піддиректорії
-   [RecursiveDirectoryIterator::key()](recursivedirectoryiterator.key.html) - Повертає шлях та ім'я файлу поточного елемента