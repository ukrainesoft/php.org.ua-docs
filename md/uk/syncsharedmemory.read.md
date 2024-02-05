---
navigation:
  - syncsharedmemory.first.md: '« SyncSharedMemory::first'
  - syncsharedmemory.size.md: 'SyncSharedMemory::size »'
  - index.md: PHP Manual
  - class.syncsharedmemory.md: SyncSharedMemory
title: 'SyncSharedMemory::read'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SyncSharedMemory::read

(PECL sync >= 1.1.0)

SyncSharedMemory::read — Копіює дані з іменованої пам'яті, що розділяється.

### Опис

```methodsynopsis
public SyncSharedMemory::read(int $start = 0, int $length = ?)
```

Копіює дані з іменованої пам'яті, що розділяється.

### Список параметрів

`start`

Початок/зміщення у байтах для початку читання.

> **Зауваження** :
> 
> Якщо значення негативне, початкова позиція буде починатися із зазначеної кількості байтів з кінця сегмента пам'яті, що розділяється.

`length`

Кількість байт для читання.

> **Зауваження** :
> 
> Якщо не вказано інше, читання зупиниться в кінці сегмента пам'яті, що розділяється.
> 
> Якщо значення негативне, читання зупиниться на зазначеній кількості байтів з кінця сегмента пам'яті, що розділяється.

### Значення, що повертаються

Рядок, що містить дані, зчитані з пам'яті, що розділяється.

### Приклади

**Пример #1 Пример использования[SyncSharedMemory::\_\_construct()](syncsharedmemory.construct.md)**

```php
<?php
// Возможно, вам потребуется защитить разделяемую память с другими объектами синхронизации.
// Разделяемая память исчезает, когда исчезает последняя ссылка на неё.
$mem = new SyncSharedMemory("AppReportName", 1024);
if ($mem->first())
{
    // Здесь можно выполнить первоначальную инициализацию.
}

$result = $mem->write("report.txt");

$result = $mem->read(3, -4);
var_dump($result);
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(3) "ort"
```

### Дивіться також

-   [SyncSharedMemory::\_\_construct()](syncsharedmemory.construct.md) \- Створює новий об'єкт SyncSharedMemory
-   [SyncSharedMemory::first()](syncsharedmemory.first.md) \- Перевіряє, чи є об'єкт першим загальносистемним екземпляром іменованої пам'яті, що розділяється.
-   [SyncSharedMemory::write()](syncsharedmemory.write.md) \- Копіює дані в іменовану пам'ять, що розділяється.
-   **SyncSharedMemory::read()**
