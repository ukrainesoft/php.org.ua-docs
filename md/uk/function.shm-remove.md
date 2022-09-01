---
navigation:
  - function.shm-remove-var.html: « shmremovevar
  - class.sysvmessagequeue.html: SysvMessageQueue »
  - index.html: PHP Manual
  - ref.sem.html: Функції семафорів
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

Сегмент пам'яті, що розділяється, отриманий з [shmattach()](function.shm-attach.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `shm` тепер чекає екземпляр [SysvSharedMemory](class.sysvsharedmemory.html); раніше очікували ресурс (resource). |

### Дивіться також

-   [shmremovevar()](function.shm-remove-var.html) - Видаляє змінну з пам'яті, що розділяється
