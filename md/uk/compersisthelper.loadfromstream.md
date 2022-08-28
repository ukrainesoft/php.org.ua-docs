Завантажує об'єкт із потоку

-   [« COMPersistHelper::LoadFromFile](compersisthelper.loadfromfile.html)
    
-   [COMPersistHelper::SaveToFile »](compersisthelper.savetofile.html)
    
-   [PHP Manual](index.html)
    
-   [COMPersistHelper](class.compersisthelper.html)
    
-   Завантажує об'єкт із потоку
    

# COMPersistHelper::LoadFromStream

(PHP 5, PHP 7, PHP 8)

COMPersistHelper::LoadFromStream — Завантажує об'єкт із потоку

### Опис

```methodsynopsis
public COMPersistHelper::LoadFromStream(resource $stream): bool
```

Завантажує об'єкт із потоку, де його спочатку було збережено.

### Список параметрів

`stream`

Потоковий ресурс для завантаження об'єкта.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викидає виняток [com\_exception](class.com-exception.html)якщо пов'язаний об'єкт не реалізує COM інтерфейс **IPersistStream**або якщо виклик **IPersistStream::Load()** завершився помилкою.