---
navigation:
  - function.shm-detach.html: « shmdetach
  - function.shm-has-var.html: shmhasvar »
  - index.md: PHP Manual
  - ref.sem.md: Функції семафорів
title: shmgetvar
---
# shmgetvar

(PHP 4, PHP 5, PHP 7, PHP 8)

shmgetvar — Повертає змінну з пам'яті, що розділяється.

### Опис

```methodsynopsis
shm_get_var(SysvSharedMemory $shm, int $key): mixed
```

**shmgetvar()** повертає змінну за ключом `key` у зазначеному сегменті пам'яті, що розділяється. Змінна все ще присутня в пам'яті, що розділяється.

### Список параметрів

`shm`

Сегмент пам'яті, що розділяється, отриманий з [shmattach()](function.shm-attach.md)

`key`

Ключ змінної.

### Значення, що повертаються

Повертає змінну із заданим ключем.

### список змін

| Версия | Описание |
| --- | --- |
|  | `shm` тепер чекає екземпляр [SysvSharedMemory](class.sysvsharedmemory.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [shmhasvar()](function.shm-has-var.md) - Перевіряє, чи існує конкретний запис
-   [shmputvar()](function.shm-put-var.md) - Вставляє або оновлює змінну в пам'яті, що розділяється.
