Зберігає об'єкт у потоці

-   [« COMPersistHelper::SaveToFile](compersisthelper.savetofile.md)
    
-   [comexception »](class.com-exception.html)
    
-   [PHP Manual](index.md)
    
-   [COMPersistHelper](class.compersisthelper.md)
    
-   Зберігає об'єкт у потоці
    

# COMPersistHelper::SaveToStream

(PHP 5, PHP 7, PHP 8)

COMPersistHelper::SaveToStream — Зберігає об'єкт у потоці

### Опис

```methodsynopsis
public COMPersistHelper::SaveToStream(resource $stream): bool
```

Зберігає об'єкт у заданому потоці.

### Список параметрів

`stream`

Потоковий ресурс.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викидає виняток [comexception](class.com-exception.html)якщо пов'язаний об'єкт не реалізує COM інтерфейс **IPersistStream**або якщо виклик **IPersistStream::Save()** завершився помилкою.