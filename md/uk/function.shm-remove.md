---
navigation:
  - function.shm-remove-var.md: « shmremovevar
  - class.sysvmessagequeue.md: SysvMessageQueue »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: shmremove
---
# shmremove

(PHP 4, PHP 5, PHP 7, PHP 8)

shmremove — Видалення пам'яті, що розділяється, з систем Unix

### Опис

```methodsynopsis
shm_remove(SysvSharedMemory $shm): bool
```

**shmremove()** видаляє пам'ять, що розділяється `shm`. Усі дані будуть знищені.

### Список параметрів

`shm`

Сегмент пам'яті, що розділяється, отриманий з [shmattach()](function.shm-attach.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `shm` тепер чекає екземпляр [SysvSharedMemory](class.sysvsharedmemory.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [shmremovevar()](function.shm-remove-var.md) - Видаляє змінну з пам'яті, що розділяється
