---
navigation:
  - function.shm-remove-var.md: « shm\_remove\_var
  - class.sysvmessagequeue.md: SysvMessageQueue »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: shm\_remove
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# shm\_remove

(PHP 4, PHP 5, PHP 7, PHP 8)

shm\_remove — Видалення пам'яті, що розділяється, з систем Unix

### Опис

```methodsynopsis
shm_remove(SysvSharedMemory $shm): bool
```

**shm\_remove()** видаляє пам'ять, що розділяється `shm`. Усі дані будуть знищені.

### Список параметрів

`shm`

Сегмент пам'яті, що розділяється, отриманий з [shm\_attach()](function.shm-attach.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `shm` тепер чекає екземпляр [SysvSharedMemory](class.sysvsharedmemory.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [shm\_remove\_var()](function.shm-remove-var.md) \- Видаляє змінну з пам'яті, що розділяється.
