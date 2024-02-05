---
navigation:
  - class.syncsharedmemory.md: « SyncSharedMemory
  - syncsharedmemory.first.md: 'SyncSharedMemory::first »'
  - index.md: PHP Manual
  - class.syncsharedmemory.md: SyncSharedMemory
title: 'SyncSharedMemory::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SyncSharedMemory::\_\_construct

(PECL sync >= 1.1.0)

SyncSharedMemory::\_\_construct — Створення нового об'єкту SyncSharedMemory

### Опис

```methodsynopsis
public SyncSharedMemory::__construct(string $name, int $size)
```

Створює іменований об'єкт пам'яті, що розділяється.

### Список параметрів

`name`

Ім'я об'єкта пам'яті, що розділяється.

> **Зауваження** :
> 
> Якщо ім'я вже існує, воно має бути доступним для відкриття поточним користувачем, від імені якого запущено процес, інакше буде викинуто виняток із безглуздим повідомленням про помилку.

`size`

Розмір в байтах пам'яті, що розділяється, яку необхідно зарезервувати.

> **Зауваження** :
> 
> Об'єм пам'яті не може бути змінено пізніше. Запитайте достатньо місця для зберігання.

### Значення, що повертаються

Новий об'єкт [SyncSharedMemory](class.syncsharedmemory.md)

### Помилки

Викидається виняток, якщо об'єкт пам'яті не може бути створений або відкритий.

### Приклади

**Пример #1 Пример использования**SyncSharedMemory::\_\_construct()\*\*\*\*

```php
<?php
// Возможно, вам потребуется защитить разделяемую память с другими объектами синхронизации.
// Разделяемая память исчезает, когда исчезает последняя ссылка на неё.
$mem = new SyncSharedMemory("AppReportName", 1024);
if ($mem->first())
{
    // Выполните здесь первоначальную инициализацию.
}

$result = $mem->write(json_encode(array("name" => "my_report.txt")));
?>
```

### Дивіться також

-   [SyncSharedMemory::first()](syncsharedmemory.first.md) \- Перевіряє, чи є об'єкт першим загальносистемним екземпляром іменованої пам'яті, що розділяється.
-   [SyncSharedMemory::size()](syncsharedmemory.size.md) \- Повертає розмір іменованої пам'яті, що розділяється
-   [SyncSharedMemory::write()](syncsharedmemory.write.md) \- Копіює дані в іменовану пам'ять, що розділяється.
-   [SyncSharedMemory::read()](syncsharedmemory.read.md) \- Копіює дані з іменованої пам'яті, що розділяється
