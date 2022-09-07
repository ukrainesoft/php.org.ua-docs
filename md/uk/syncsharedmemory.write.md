---
navigation:
  - syncsharedmemory.size.md: '« SyncSharedMemory::size'
  - refs.basic.other.md: Інші базові модулі »
  - index.md: PHP Manual
  - class.syncsharedmemory.md: SyncSharedMemory
title: 'Sync Shared Memory::write'
---
# Sync Shared Memory::write

(PECL sync >= 1.1.0)

Sync Shared Memory::write — Копіює дані в іменовану пам'ять, що розділяється.

### Опис

```methodsynopsis
public SyncSharedMemory::write(string $string = ?, int $start = 0)
```

Копіює дані в іменовану пам'ять, що розділяється.

### Список параметрів

`string`

Дані для запису в пам'ять, що розділяється.

> **Зауваження**
> 
> Якщо розмір даних перевищує розмір пам'яті, що розділяється, кількість записаних повертаються байтів буде менше довжини вхідних даних.

`start`

Початок/зміщення у байтах для початку запису.

> **Зауваження**
> 
> Якщо значення негативне, початкова позиція буде починатися із зазначеної кількості байтів з кінця сегмента пам'яті, що розділяється.

### Значення, що повертаються

Ціле число, що містить кількість байтів, записаних у пам'ять, що розділяється.

### Приклади

**Приклад #1 Приклад використання **Sync Shared Memory::write()****

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
var_dump($result);

$result = $mem->write("report.txt", -3);
var_dump($result);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(10)
int(3)
```

### Дивіться також

-   [SyncSharedMemory::construct()](syncsharedmemory.construct.md) - Створює новий об'єкт SyncSharedMemory
-   [SyncSharedMemory::first()](syncsharedmemory.first.md) - Перевіряє, чи є об'єкт першим загальносистемним екземпляром іменованої пам'яті, що розділяється.
-   **Sync Shared Memory::write()**
-   [SyncSharedMemory::read()](syncsharedmemory.read.md) - Копіює дані з іменованої пам'яті, що розділяється
