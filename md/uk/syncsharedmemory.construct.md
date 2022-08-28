Створює новий об'єкт SyncSharedMemory

-   [« SyncSharedMemory](class.syncsharedmemory.html)
    
-   [SyncSharedMemory::first »](syncsharedmemory.first.html)
    
-   [PHP Manual](index.html)
    
-   [SyncSharedMemory](class.syncsharedmemory.html)
    
-   Створює новий об'єкт SyncSharedMemory
    

# SyncSharedMemory::construct

(PECL sync >= 1.1.0)

SyncSharedMemory::construct — Створення нового об'єкту SyncSharedMemory

### Опис

```methodsynopsis
public SyncSharedMemory::__construct(string $name, int $size)
```

Створює іменований об'єкт пам'яті, що розділяється.

### Список параметрів

`name`

Ім'я об'єкта пам'яті, що розділяється.

> **Зауваження**
> 
> Якщо ім'я вже існує, воно має бути доступним для відкриття поточним користувачем, від імені якого запущено процес, інакше буде викинуто виняток із безглуздим повідомленням про помилку.

`size`

Розмір в байтах пам'яті, що розділяється, яку необхідно зарезервувати.

> **Зауваження**
> 
> Об'єм пам'яті не може бути змінено пізніше. Запитайте достатньо місця для зберігання.

### Значення, що повертаються

Новий об'єкт [SyncSharedMemory](class.syncsharedmemory.html)

### Помилки

Викидається виняток, якщо об'єкт пам'яті не може бути створений або відкритий.

### Приклади

**Приклад #1 Приклад використання **SyncSharedMemory::construct()****

```php
<?php
// Возможно, вам потребуется защитить разделяемую память с другими объектами синхронизации.
// Разделяемая память исчезает, когда исчезает последняя ссылка на неё.
$mem = new SyncSharedMemory("AppReportName", 1024);
if ($mem->first())
{
    // Выполните здесь первоначальную инициализацию.
}

$result = $mem->write(json_encode(array("name" => "my_report.txt")));
?>
```

### Дивіться також

-   [SyncSharedMemory::first()](syncsharedmemory.first.html) - Перевіряє, чи є об'єкт першим загальносистемним екземпляром іменованої пам'яті, що розділяється.
-   [SyncSharedMemory::size()](syncsharedmemory.size.html) - Повертає розмір іменованої пам'яті, що розділяється
-   [SyncSharedMemory::write()](syncsharedmemory.write.html) - Копіює дані в іменовану пам'ять, що розділяється.
-   [SyncSharedMemory::read()](syncsharedmemory.read.html) - Копіює дані з іменованої пам'яті, що розділяється