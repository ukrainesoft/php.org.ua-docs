Отримати максимальний розмір потоку

-   [« COMPersistHelper::GetCurFileName](compersisthelper.getcurfilename.html)
    
-   [COMPersistHelper::InitNew »](compersisthelper.initnew.html)
    
-   [PHP Manual](index.html)
    
-   [COMPersistHelper](class.compersisthelper.html)
    
-   Отримати максимальний розмір потоку
    

# COMPersistHelper::GetMaxStreamSize

(PHP 5, PHP 7, PHP 8)

COMPersistHelper::GetMaxStreamSize — Отримати максимальний розмір потоку

### Опис

```methodsynopsis
public COMPersistHelper::GetMaxStreamSize(): int
```

Повертає розмір потоку (в байтах), необхідний збереження об'єкта.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає розмір потоку (в байтах), необхідний збереження об'єкта.

### Помилки

Викидає виняток [com\_exception](class.com-exception.html)якщо пов'язаний об'єкт не реалізує COM інтерфейс **IPersistStreamInit**або якщо виклик **IPersistStream::GetSizeMax()** завершився помилкою.