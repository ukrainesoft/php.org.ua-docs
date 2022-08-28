Отримати ім'я файлу

-   [« COMPersistHelper::\_\_construct](compersisthelper.construct.html)
    
-   [COMPersistHelper::GetMaxStreamSize »](compersisthelper.getmaxstreamsize.html)
    
-   [PHP Manual](index.html)
    
-   [COMPersistHelper](class.compersisthelper.html)
    
-   Отримати ім'я файлу
    

# COMPersistHelper::GetCurFileName

(PHP 5, PHP 7, PHP 8)

COMPersistHelper::GetCurFileName — Отримати ім'я файлу

### Опис

```methodsynopsis
public COMPersistHelper::GetCurFileName(): string|false
```

Повертає назву файлу, пов'язаного з об'єктом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я файлу, пов'язаного з об'єктом.

### Помилки

Викидає виняток [com\_exception](class.com-exception.html)якщо пов'язаний об'єкт не реалізує COM інтерфейс **IPersistFile**або якщо виклик **IPersistFile::GetCurFile()** завершився помилкою.