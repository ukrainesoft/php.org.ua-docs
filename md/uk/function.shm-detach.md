---
navigation:
  - function.shm-attach.md: « shm\_attach
  - function.shm-get-var.md: shm\_get\_var »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: shm\_detach
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# shm\_detach

(PHP 4, PHP 5, PHP 7, PHP 8)

shm\_detach — Відключається від сегмента пам'яті, що розділяється.

### Опис

```methodsynopsis
shm_detach(SysvSharedMemory $shm): bool
```

**shm\_detach()** відключається від сегмента пам'яті, що розділяється, вказаного в `shm`, созданного[shm\_attach()](function.shm-attach.md). Пам'ятайте, що пам'ять, що розділяється, все ще існує в системі Unix і дані все ще присутні.

### Список параметрів

`shm`

Сегмент пам'яті, що розділяється, отриманий з [shm\_attach()](function.shm-attach.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `shm` чекає на екземпляр [SysvSharedMemory](class.sysvsharedmemory.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [shm\_attach()](function.shm-attach.md) \- Створює або відкриває сегмент пам'яті, що розділяється
-   [shm\_remove()](function.shm-remove.md) \- Видаляє пам'ять, що розділяється, з систем Unix
-   [shm\_remove\_var()](function.shm-remove-var.md) \- Видаляє змінну з пам'яті, що розділяється.
