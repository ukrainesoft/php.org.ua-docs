---
navigation:
  - function.shm-attach.md: « shmattach
  - function.shm-get-var.md: shmgetvar »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: shmdetach
---
# shmdetach

(PHP 4, PHP 5, PHP 7, PHP 8)

shmdetach — Вимикається від сегмента пам'яті, що розділяється.

### Опис

```methodsynopsis
shm_detach(SysvSharedMemory $shm): bool
```

**shmdetach()** відключається від сегмента пам'яті, зазначеного в `shm`, створеного [shmattach()](function.shm-attach.md). Пам'ятайте, що пам'ять, що розділяється, все ще існує в системі Unix і дані все ще присутні.

### Список параметрів

`shm`

Сегмент пам'яті, що розділяється, отриманий з [shmattach()](function.shm-attach.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `shm` чекає на екземпляр [SysvSharedMemory](class.sysvsharedmemory.md); раніше очікувався ресурс (resource). |

### Дивіться також

-   [shmattach()](function.shm-attach.md) - Створює або відкриває сегмент пам'яті, що розділяється
-   [shmremove()](function.shm-remove.md) - Видаляє пам'ять, що розділяється, з систем Unix
-   [shmremovevar()](function.shm-remove-var.md) - Видаляє змінну з пам'яті, що розділяється.
