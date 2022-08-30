Якщо поточний елемент є директорією, метод повертає нею ітератор

-   [« RecursiveDirectoryIterator::construct](recursivedirectoryiterator.construct.html)
    
-   [RecursiveDirectoryIterator::getSubPath »](recursivedirectoryiterator.getsubpath.html)
    
-   [PHP Manual](index.html)
    
-   [RecursiveDirectoryIterator](class.recursivedirectoryiterator.html)
    
-   Якщо поточний елемент є директорією, метод повертає нею ітератор
    

# RecursiveDirectoryIterator::getChildren

(PHP 5> = 5.1.0, PHP 7, PHP 8)

RecursiveDirectoryIterator::getChildren - Якщо поточний елемент є директорією, метод повертає для неї ітератор

### Опис

```methodsynopsis
public RecursiveDirectoryIterator::getChildren(): RecursiveDirectoryIterator
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ім'я файлу, інформація про файл або посилання на об'єкт $this. Що саме повертатиметься залежить від прапорів налаштувань. Дивіться додатково [Константи FilesystemIterator](class.filesystemiterator.html#filesystemiterator.constants)